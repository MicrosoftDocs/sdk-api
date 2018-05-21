---
UID: TP:wincontacts
ms.assetid: e0e7bda2-6a92-33f7-a8e7-cf235874dd82
ms.author: windowsdriverdev
ms.date: 05/21/18
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: portal
archived: true
---

# Windows Contacts



Overview of the Windows Contacts technology.

To develop Windows Contacts, you need these headers:

 * [icontact.h](..\icontact\index.md)

For the programming guide, see [Windows Contacts](https://review.docs.microsoft.com/en-us/win32-test/wincontacts).

## Interfaces

| Title   | Description   |
| ---- |:---- |
| [IContact interface](..\icontact\nn-icontact-icontact.md) | Do not use. Defines methods for reading and writing properties for a single contact. |
| [IContactCollection interface](..\icontact\nn-icontact-icontactcollection.md) | Do not use. Enumerates the contacts known by the IContactManager. |
| [IContactManager interface](..\icontact\nn-icontact-icontactmanager.md) | Do not use. Used for retrieving a contact, based on a contact ID string. |
| [IContactProperties interface](..\icontact\nn-icontact-icontactproperties.md) | Do not use. Used to retrieve, set, create, and remove properties on an IContact. Property names and extension mechanisms are described in icontactproperties.h. |
| [IContactPropertyCollection interface](..\icontact\nn-icontact-icontactpropertycollection.md) | Do not use. Used to filter contact data, based on a label or property set. Enumerates contact properties exposed with an IContactProperties object. For each property, the name, type, version, and modification date can be retrieved. |

## Methods

| Title   | Description   |
| ---- |:---- |
| [IContact::CommitChanges](..\icontact\nf-icontact-icontact-commitchanges.md) | Saves changes made to this contact to the contact file. |
| [IContact::GetContactID](..\icontact\nf-icontact-icontact-getcontactid.md) | Retrieves the local computer unique contact ID. |
| [IContact::GetPath](..\icontact\nf-icontact-icontact-getpath.md) | Retrieves the file system path used to load this contact. |
| [IContactCollection::GetCurrent](..\icontact\nf-icontact-icontactcollection-getcurrent.md) | Retrieves the current contact in the enumeration. |
| [IContactCollection::Next](..\icontact\nf-icontact-icontactcollection-next.md) | Moves to the next contact. |
| [IContactCollection::Reset](..\icontact\nf-icontact-icontactcollection-reset.md) | Resets the enumerator to before the logical first element. |
| [IContactManager::GetContactCollection](..\icontact\nf-icontact-icontactmanager-getcontactcollection.md) | Returns an IContactCollection object that contains all known contacts. |
| [IContactManager::GetMeContact](..\icontact\nf-icontact-icontactmanager-getmecontact.md) | Retrieves the local user account concept of 'me'. |
| [IContactManager::Initialize](..\icontact\nf-icontact-icontactmanager-initialize.md) | Initializes the contact manager with the unique application name and application version being used to manipulate contacts. |
| [IContactManager::Load](..\icontact\nf-icontact-icontactmanager-load.md) | Loads an IContact object with the data from the contact referenced by the computer-local contact ID. |
| [IContactManager::MergeContactIDs](..\icontact\nf-icontact-icontactmanager-mergecontactids.md) | Makes an old Contact ID resolve to the same value as a new Contact ID. Subsequent calls to IContactManager |
| [IContactManager::SetMeContact](..\icontact\nf-icontact-icontactmanager-setmecontact.md) | Sets the local user account concept of 'me' to specified user. |
| [IContactProperties::CreateArrayNode](..\icontact\nf-icontact-icontactproperties-createarraynode.md) | Creates a new array node in a multi-value property. |
| [IContactProperties::DeleteArrayNode](..\icontact\nf-icontact-icontactproperties-deletearraynode.md) | Deletes the data at a specified array entry. |
| [IContactProperties::DeleteLabels](..\icontact\nf-icontact-icontactproperties-deletelabels.md) | Deletes the labels at a specified array entry. |
| [IContactProperties::DeleteProperty](..\icontact\nf-icontact-icontactproperties-deleteproperty.md) | Deletes the value at a specified property. Property modification and version data can still be enumerated with IContactPropertyCollection. |
| [IContactProperties::GetBinary](..\icontact\nf-icontact-icontactproperties-getbinary.md) | Retrieves the binary data of a property using an IStream interface [Structured Storage]. |
| [IContactProperties::GetDate](..\icontact\nf-icontact-icontactproperties-getdate.md) | Retrieves the date and time value at a specified property into a caller's FILETIME structure. All times are stored and returned as Coordinated Universal Time (UTC). |
| [IContactProperties::GetLabels](..\icontact\nf-icontact-icontactproperties-getlabels.md) | Retrieves the labels for a specified array element name. |
| [IContactProperties::GetPropertyCollection](..\icontact\nf-icontact-icontactproperties-getpropertycollection.md) | Returns an IContactPropertyCollection for the current contact. Optionally, filters the IContactPropertyCollection to enumerate only some values. |
| [IContactProperties::GetString](..\icontact\nf-icontact-icontactproperties-getstring.md) | Retrieves the string value at a specified property into a caller-allocated buffer. |
| [IContactProperties::SetBinary](..\icontact\nf-icontact-icontactproperties-setbinary.md) | Sets the binary data at a specified property to the contents of a specified IStream interface [Structured Storage], which contains a null-terminated string (as MIME type) data. |
| [IContactProperties::SetDate](..\icontact\nf-icontact-icontactproperties-setdate.md) | Sets the date and time value at a specified property to a given FILETIME. All times are stored and returned as Coordinated Universal Time (UTC). |
| [IContactProperties::SetLabels](..\icontact\nf-icontact-icontactproperties-setlabels.md) | Appends the set of labels passed in to the specified property's label set. Note |
| [IContactProperties::SetString](..\icontact\nf-icontact-icontactproperties-setstring.md) | Sets the string value of a specified property to that of a specified null-terminated string. |
| [IContactPropertyCollection::GetPropertyArrayElementID](..\icontact\nf-icontact-icontactpropertycollection-getpropertyarrayelementid.md) | Retrieves the unique ID for a given element in a property array. |
| [IContactPropertyCollection::GetPropertyModificationDate](..\icontact\nf-icontact-icontactpropertycollection-getpropertymodificationdate.md) | Retrieves the last modification date for the current property in the enumeration. If not modified, contact creation date is returned. |
| [IContactPropertyCollection::GetPropertyName](..\icontact\nf-icontact-icontactpropertycollection-getpropertyname.md) | Retrieves the name for the current property in the enumeration. |
| [IContactPropertyCollection::GetPropertyType](..\icontact\nf-icontact-icontactpropertycollection-getpropertytype.md) | Retrieves the type for the current property in the enumeration. |
| [IContactPropertyCollection::GetPropertyVersion](..\icontact\nf-icontact-icontactpropertycollection-getpropertyversion.md) | Retrieves the version number for the current property in the enumeration. |
| [IContactPropertyCollection::Next](..\icontact\nf-icontact-icontactpropertycollection-next.md) | Moves to the next property. |
| [IContactPropertyCollection::Reset](..\icontact\nf-icontact-icontactpropertycollection-reset.md) | Resets enumeration of properties. |
