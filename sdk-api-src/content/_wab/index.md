---
UID: TP:wab
ms.assetid: 56a65500-d04e-3d2e-85d2-62accfb13a81
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: 
ms.prod: windows
ms.technology: windows-sdk
ms.topic: portal
archived: true
---

# Windows Address Book



Overview of the Windows Address Book technology.

To develop Windows Address Book, you need these headers:

 * [wabapi.h](..\wabapi\index.md)
 * [wabdefs.h](..\wabdefs\index.md)
 * [wabiab.h](..\wabiab\index.md)
 * [wabtags.h](..\wabtags\index.md)

For the programming guide, see [Windows Address Book](/previous-versions/windows/desktop/wab).

## Callback functions

| Title   | Description   |
| ---- |:---- |
| [WABOpen callback function](..\wabapi\nc-wabapi-wabopen.md) | Do not use. Provides access to the address book through a number of object interfaces. The root interface is IAddrBook, which is a subset of the MAPI implementation of IAddrBook. |
| [WABOpenEx callback function](..\wabapi\nc-wabapi-wabopenex.md) | WABOpenEx is no longer available for use as of Windows Vista. |

## Structures

| Title   | Description   |
| ---- |:---- |
| [ENTRYID structure](..\wabdefs\ns-wabdefs-entryid.md) | Do not use. Contains the entry identifier information for a MAPI object. |
| [_ADRENTRY structure](..\wabdefs\ns-wabdefs-_adrentry.md) | Do not use. Describes zero or more properties belonging to one or more recipients. |
| [_ADRLIST structure](..\wabdefs\ns-wabdefs-_adrlist.md) | Do not use. Describes zero or more properties belonging to one or more recipients. |
| [_ADRPARM structure](..\wabdefs\ns-wabdefs-_adrparm.md) | Do not use. Describes the display and behavior of the common address dialog box. |
| [_SBinaryArray structure](..\wabdefs\ns-wabdefs-_sbinaryarray.md) | Do not use. An array of entry identifiers representing MAPI objects. Uses the same implementation as SBinaryArray. |
| [_SPropProblem structure](..\wabdefs\ns-wabdefs-_spropproblem.md) | Do not use. Describes an error relating to an operation involving a property. |
| [_SPropProblemArray structure](..\wabdefs\ns-wabdefs-_spropproblemarray.md) | Do not use. Contains an array of one or more SPropProblem structures. |
| [_SPropTagArray structure](..\wabdefs\ns-wabdefs-_sproptagarray.md) | Do not use. Contains an array of property tags. |
| [_SPropValue structure](..\wabdefs\ns-wabdefs-_spropvalue.md) | Do not use. Contains the property tag values. |
| [_SRestriction structure](..\wabdefs\ns-wabdefs-_srestriction.md) | Do not use. Describes a filter for limiting the view of a table to particular rows. |
| [_SRow structure](..\wabdefs\ns-wabdefs-_srow.md) | Do not use. Describes a row from a table containing selected properties for a specific object. |
| [_SRowSet structure](..\wabdefs\ns-wabdefs-_srowset.md) | Do not use. Contains an array of SRow structures. Each SRow structure describes a row from a table. |
| [_SSortOrder structure](..\wabdefs\ns-wabdefs-_ssortorder.md) | Do not use. Defines how to sort rows of a table, describing both the column to use as the sort key and the direction of the sort. |
| [_SSortOrderSet structure](..\wabdefs\ns-wabdefs-_ssortorderset.md) | Do not use. Defines a collection of keys for a table to be used for standard or categorized sorting. |
| [_WABEXTDISPLAY structure](..\wabapi\ns-wabapi-_wabextdisplay.md) | Do not use. Used by the Windows Address Book (WAB) to initialize user's IContextMenu Interface and IShellPropSheetExt Interface implementations. |
| [_WABIMPORTPARAM structure](..\wabapi\ns-wabapi-_wabimportparam.md) | Do not use. Structure passed to Import that gives information about importing .wab files. |
| [_tagWAB_PARAM structure](..\wabapi\ns-wabapi-_tagwab_param.md) | Do not use. Contains the input information to pass to WABOpen. |

## Enumerations

| Title   | Description   |
| ---- |:---- |
| [Gender enumeration](..\wabtags\ne-wabtags-gender.md) | Do not use. The Gender enumeration specifies the possible values for the PR_GENDER property. |

## Interfaces

| Title   | Description   |
| ---- |:---- |
| [IABContainer interface](..\wabdefs\nn-wabdefs-iabcontainer.md) | Do not use. This interface provides access to address book containers. Applications call the methods of the interface to perform name resolution and to create, copy, and delete recipients. |
| [IAddrBook interface](..\wabiab\nn-wabiab-iaddrbook.md) | Do not use. |
| [IDistList interface](..\wabdefs\nn-wabdefs-idistlist.md) | Do not use. This interface is used to provide access to distribution lists in modifiable address book containers. The interface provides methods to create, copy, and delete distribution lists, in addition to performing name resolution. |
| [IMAPITable interface](..\wabdefs\nn-wabdefs-imapitable.md) | Do not use. This interface is used for content tables of Windows Address Book (WAB) containers and distribution lists. |
| [IMailUser interface](..\wabdefs\nn-wabdefs-imailuser.md) | Do not use. This interface provides access to a mail user object. |
| [IWABExtInit interface](..\wabapi\nn-wabapi-iwabextinit.md) | Do not use. This interface ndicates which Windows Address Book (WAB) object is being displayed (for example, a property sheet or context menu). |
| [IWABObject interface](..\wabapi\nn-wabapi-iwabobject.md) | Do not use. This interface provides access to the Windows Address Book (WAB) object which contains function pointers to memory allocation functions and database maintenance functions. |
