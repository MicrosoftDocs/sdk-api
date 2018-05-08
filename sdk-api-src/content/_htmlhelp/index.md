---
UID: TP:htmlhelp
ms.assetid: adfbbda2-b7ca-3f58-bd38-3aaccbf29126
ms.author: windowsdriverdev
ms.date: 05/07/18
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: portal
---

# Microsoft HTML Help 1.4



Overview of the Microsoft HTML Help 1.4 technology.

To develop Microsoft HTML Help 1.4, you need these headers:

 * [htmlhelp.h](..\htmlhelp\index.md)
 * [infotech.h](..\infotech\index.md)

For the programming guide, see [Microsoft HTML Help 1.4](https://review.docs.microsoft.com/en-us/win32-test/htmlhelp).

## Functions

| Title   | Description   |
| ---- |:---- |
| [HtmlHelpA function](..\htmlhelp\nf-htmlhelp-htmlhelpa.md) | Displays a help window. |
| [HtmlHelpW function](..\htmlhelp\nf-htmlhelp-htmlhelpw.md) | Displays a help window. |

## Structures

| Title   | Description   |
| ---- |:---- |
| [tagHHNTRACK structure](..\htmlhelp\ns-htmlhelp-taghhntrack.md) | This structure returns the file name of the current topic and a constant that specifies the user action that is about to occur, such as hiding the Navigation pane by clicking the Hide button on the toolbar. |
| [tagHHN_NOTIFY structure](..\htmlhelp\ns-htmlhelp-taghhn_notify.md) | Use this structure to return the file name of the topic that has been navigated to, or to return the window type name of the help window that has been created. |
| [tagHH_AKLINK structure](..\htmlhelp\ns-htmlhelp-taghh_aklink.md) | Use this structure to specify one or more ALink names or KLink keywords that you want to search for. |
| [tagHH_FTS_QUERY structure](..\htmlhelp\ns-htmlhelp-taghh_fts_query.md) | Use this structure for full-text search. |
| [tagHH_POPUP structure](..\htmlhelp\ns-htmlhelp-taghh_popup.md) | Use this structure to specify or modify the attributes of a pop-up window. |
| [tagHH_WINTYPE structure](..\htmlhelp\ns-htmlhelp-taghh_wintype.md) | Use this structure to specify or modify the attributes of a window type. |

## Interfaces

| Title   | Description   |
| ---- |:---- |
| [IITDatabase interface](..\infotech\nn-infotech-iitdatabase.md) | Use this interface for opening and closing the database object, and for instantiating objects stored in the database. |
| [IITPropList interface](..\infotech\nn-infotech-iitproplist.md) | Use this interface to set properties for build objects such as word wheels and indexes. Call these methods in the document build process to define properties for all build objects. |
| [IITResultSet interface](..\infotech\nn-infotech-iitresultset.md) | Use this interface in run-time applications to initialize, build, and obtain information about result sets. |
| [IITWordWheel interface](..\infotech\nn-infotech-iitwordwheel.md) | Use this interface to perform word wheel keyword lookups. The Lookup method offers several ways of performing a search |
| [IStemmerConfig interface](..\infotech\nn-infotech-istemmerconfig.md) | Use this interface to provide configuration information that controls stemming. |

## Methods

| Title   | Description   |
| ---- |:---- |
| [IITDatabase::Close](..\infotech\nf-infotech-iitdatabase-close.md) | Closes a database. |
| [IITDatabase::CreateObject](..\infotech\nf-infotech-iitdatabase-createobject.md) | Creates an unnamed object you can reference in the future through the *pdwObjInstance parameter. |
| [IITDatabase::GetObject](..\infotech\nf-infotech-iitdatabase-getobject.md) | Retrieves a specified IUnknown-based interface on the object identified by the dwObjInstance parameter. |
| [IITDatabase::Open](..\infotech\nf-infotech-iitdatabase-open.md) | Opens a database. |
| [IITPropList::Clear](..\infotech\nf-infotech-iitproplist-clear.md) | Clears memory associated with a property list and reinitializes the list. |
| [IITPropList::GetDataSize](..\infotech\nf-infotech-iitproplist-getdatasize.md) | Returns the number of bytes needed to save the property data. |
| [IITPropList::GetFirst](..\infotech\nf-infotech-iitproplist-getfirst.md) | Returns the first property object in a property list. |
| [IITPropList::GetHeaderSize](..\infotech\nf-infotech-iitproplist-getheadersize.md) | Returns the number of bytes needed to save the header. |
| [IITPropList::Get](..\infotech\nf-infotech-iitproplist-get.md) | Returns the property object associated with the given property ID. |
| [IITPropList::SaveData](..\infotech\nf-infotech-iitproplist-savedata.md) | Saves the data size and data from the property list to a buffer. |
| [IITPropList::SaveHeader](..\infotech\nf-infotech-iitproplist-saveheader.md) | Saves the property ID and data type from the property list to a buffer. Only saves properties marked with a persistence state of TRUE. |
| [IITPropList::Set method](..\infotech\nf-infotech-iitproplist-set.md) | Sets a property to a given value or deletes a property from the list. |
| [IITPropList::Set(PROPID,DWORD,DWORD)](..\infotech\nf-infotech-iitproplist-set(propid,dword,dword).md) | Sets a property to a given value or deletes a property from the list. |
| [IITPropList::Set(PROPID,LPCWSTR,DWORD)](..\infotech\nf-infotech-iitproplist-set(propid,lpcwstr,dword).md) | Sets a property to a given value or deletes a property from the list. |
| [IITPropList::Set(PROPID,LPVOID,DWORD,DWORD)](..\infotech\nf-infotech-iitproplist-set(propid,lpvoid,dword,dword).md) | Sets a property to a given value or deletes a property from the list. |
| [IITPropList::SetPersist(BOOL)](..\infotech\nf-infotech-iitproplist-setpersist(bool).md) | Sets the persistence state on or off for all properties. |
| [IITPropList::SetPersist](..\infotech\nf-infotech-iitproplist-setpersist.md) | Sets the persistence state on or off for a given property. |
| [IITResultSet::Add method](..\infotech\nf-infotech-iitresultset-add.md) | Adds columns to result set, given a header containing pairs of property ID followed by property type. |
| [IITResultSet::Add(LPVOID)](..\infotech\nf-infotech-iitresultset-add(lpvoid).md) | Adds columns to result set, given a header containing pairs of property ID followed by property type. |
| [IITResultSet::Add(PROPID,DWORD,PRIORITY)](..\infotech\nf-infotech-iitresultset-add(propid,dword,priority).md) | Adds a column to the result set. |
| [IITResultSet::Add(PROPID,LPCWSTR,PRIORITY)](..\infotech\nf-infotech-iitresultset-add(propid,lpcwstr,priority).md) | Adds a column to the result set. |
| [IITResultSet::Add(PROPID,LPVOID,DWORD,PRIORITY)](..\infotech\nf-infotech-iitresultset-add(propid,lpvoid,dword,priority).md) | Adds a column to the result set. |
| [IITResultSet::GetRowCount](..\infotech\nf-infotech-iitresultset-getrowcount.md) | Gets the number of rows in a result set. |
| [IITResultSet::Get](..\infotech\nf-infotech-iitresultset-get.md) | Gets the property in the specified row and column and fills the given property object. |
| [IITWordWheel::Close](..\infotech\nf-infotech-iitwordwheel-close.md) | Closes a word wheel. |
| [IITWordWheel::Count](..\infotech\nf-infotech-iitwordwheel-count.md) | Returns the number of entries in a word wheel. |
| [IITWordWheel::Lookup method](..\infotech\nf-infotech-iitwordwheel-lookup.md) | Looks up an entry and returns contents in a buffer. |
| [IITWordWheel::Lookup(LONG,IITResultSet,LONG)](..\infotech\nf-infotech-iitwordwheel-lookup(long,iitresultset,long).md) | Looks up an entry and returns contents in a buffer. |
| [IITWordWheel::Lookup(LONG,LPVOID,DWORD)](..\infotech\nf-infotech-iitwordwheel-lookup(long,lpvoid,dword).md) | Looks up an entry and returns contents in a buffer. |
| [IITWordWheel::Lookup(LPCVOID,BOOL,LONG)](..\infotech\nf-infotech-iitwordwheel-lookup(lpcvoid,bool,long).md) | Looks up an entry and returns contents in a buffer. |
| [IITWordWheel::Open](..\infotech\nf-infotech-iitwordwheel-open.md) | Opens a word wheel. |
| [IStemmerConfig::SetLocaleInfo](..\infotech\nf-infotech-istemmerconfig-setlocaleinfo.md) | Sets locale information for the stemmer. |
