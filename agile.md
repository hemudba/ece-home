# Agile

We're in the process of rolling out an Agile framework for helping us develop our software. The information here is subject
to change as the process evolves.

## How We Work

Read [this documentation](./how-we-work.md) to get an understanding of our methodologies. This will walk you through what
project management tools we use, which meetings occur when and where, and general expectations from team members.

Keep in mind that this is not a process that is set in stone; we welcome all feedback for improvements!

## For Developers

It's useful to keep track of the context behind changes that go into our source code. This has many benefits, in particular
allowing a developer to view the Git history, find relevant pull requests and then see what Rally work items they originated
from. Previously, this was done by referencing a GitHub issue.

To that extent, there are some integrations that can help connect GitHub and Rally at a very lightweight level.

Rally stories are named using a well-known convention. Stories start with a `US` (user story) prefix, followed by numbers. These
identifiers are unique to the tenancy, meaning that a story number will never collide with another team's story in UHG. A full
example would be `US152322`.

### Autolinks


To facilitate linking GitHub to Rally, we can set up an autolink reference on a per-repository basis.

This can be found in repository Settings -> Autolink References.
![image](https://github.optum.com/storage/user/167/files/d18de9cd-a303-4a69-807e-651c568ecc78)

* Use a numeric rule
* Set the prefix to `US`
* Set the target URL to `https://rally1.rallydev.com/#/search?keywords=US<num>`

Now when a developer puts a story number in a pull request comment, GitHub will automatically generate a link directly to
Rally.

**Note**: setting this up at the organization level is [not yet supported](https://github.com/community/community/discussions/12386).

## Future Enhancements

Once we mature as an Agile team, we can look into more deeply integrated setups using something like a [Rally GitHub app](https://github.com/github/rally)
to provide additional functionality. This is more heavy weight in the sense that we could set up pull request checks to require stories
be in particular states, bugs are closed out, etc.
