---
title: DNN API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - powershell
  - csharp
  - vb
  - javascript

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/lord/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to the DNN Developer Documentation Site. DNN is a great platform for developing .NET web applications as 
well as full support for modern Single Page Applications (SPA). Whether you build in ReactJS, VueJS, or vanilla JS, 
you'll be able to build secure, robust applications.

This documentation is intended to provide developers with all the information they need to get solutions running quickly. 
At the same time, it provides an in-depth reference to the DNN API.

# Concepts
### Entities, Info Objects and Controllers
When navigating the API, you'll find most of your work involves Controllers acting on Info objects. Info objects 
typically describe individual items such as a User, Page (called a Tab in the API for historical reasons), Portal, etc.
Many of these objects can be found in the `DotNetNuke.Entities` namespace.

### Plug-in Components
Many aspects of DNN are capable of using drop-in replacements, enabling you to highly customize how certain aspects of 
the site, like authentication, work. This is accomplished using the [Provider pattern](http://somelink.here)


# Users
Users are central to development within DNN. The core object you'll be working with is the `UserInfo` object
## Adding a User to a Portal

## Getting a User

## Listing Users

## Deleting a User



## UserInfo Class
```csharp
[SerializableAttribute]
public class UserInfo : BaseEntityInfo, IPropertyAccess
```
```vb
<SerializableAttribute>
Public Class UserInfo
	Inherits BaseEntityInfo
	Implements IPropertyAccess
```
The `UserInfo` class contains all the data that describes a user in the DNN system.

### Methods
Name | Description 
---- | -----------
`ClearRoles` | Obsolete as of version 99.99.99
`CloneBaseProperties` | (Inherited from BaseEntityInfo)
`CreatedByUser` | Gets the UserInfo object associated with this User (Inherited from BaseEntityInfo)
`IsInRole` | Determines if the user is in the passed-in role

### IsInRole
```csharp
public bool IsInRole(
	string role
)
```
```vb
Public Function IsInRole ( 
	role As String
) As Boolean
```
Pass a [role name](https://somelink.com/#list-roles) into the function. It will return a Boolean (True/False) value indicating if the user 
is in that role


