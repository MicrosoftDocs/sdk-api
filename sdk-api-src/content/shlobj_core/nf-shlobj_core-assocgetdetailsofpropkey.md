---
UID: NF:shlobj_core.AssocGetDetailsOfPropKey
title: AssocGetDetailsOfPropKey function
author: windows-sdk-content
description: Retrieves the value for a given property key using the file association information provided by the Namespace Extensions.
old-location: shell\AssocGetDetailsOfPropKey.htm
old-project: shell
ms.assetid: f13af5f4-1b6a-419c-a042-e05c9ec51d02
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: AssocGetDetailsOfPropKey, AssocGetDetailsOfPropKey function [Windows Shell], _shell_AssocGetDetailsOfPropKey, shell.AssocGetDetailsOfPropKey, shlobj_core/AssocGetDetailsOfPropKey
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: AUTOCOMPLETELISTOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
 - API-MS-Win-Shell-Associations-L1-1-0.dll
 - Windows.Storage.dll
api_name:
 - AssocGetDetailsOfPropKey
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Internet Explorer 5.0
---

# AssocGetDetailsOfPropKey function


## -description


Retrieves the value for a given property key using the file association information provided by the <a href="https://msdn.microsoft.com/cc387338-15fa-4350-b039-61a0f1c5030a">Namespace Extensions</a>.


## -parameters




### -param psf [in]

Type: <b><a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a>*</b>

A pointer to the shell folder for which the details of the property key of the file association are being retrieved.


### -param pidl [in]

Type: <b>PCUITEMID_CHILD</b>

The PIDL of the child item for which the file associations are being requested.


### -param pkey [in]

Type: <b><a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a>*</b>

A pointer to the property key that is being retrieved.


### -param pv [out]

Type: <b>VARIANT*</b>

When this function returns, contains the details of the given property key.


### -param pfFoundPropKey [out]

Type: <b>BOOL*</b>

When this function returns, contains a flag that is <b>TRUE</b> if the property key was found, otherwise <b>FALSE</b>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function is to be used only by implementers of 
     <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a> <a href="https://msdn.microsoft.com/cc387338-15fa-4350-b039-61a0f1c5030a">Namespace Extensions</a>. Other calling applications should use 
     <a href="https://msdn.microsoft.com/f006828c-980d-4e36-be68-3b3c238cd884">IShellFolder2::GetDetailsEx</a> to get a value 
     for a <a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a>. This function is to be used by 
     implementers of <b>IShellFolder</b> Namespace Extensions.

The provided namespace extension must support the use of this API in one of the following three ways.

<ol>
<li>If the provided <a href="https://msdn.microsoft.com/cc387338-15fa-4350-b039-61a0f1c5030a">Namespace Extensions</a> supports retrieving an <a href="https://msdn.microsoft.com/8edb99d3-5860-4d78-a750-1df34cdfc313">IQueryAssociations</a> interface for the item by implementing <a href="https://msdn.microsoft.com/ec863dbf-8ec9-4952-8912-575125e6dd09">IShellFolder::GetUIObjectOf</a>(..., <b>IID_IQueryAssociations</b>, ...), then <b>AssocGetDetailsOfPropKey</b> will use the provided file associations API to retrieve the value for the property key.</li>
<li>If the provided namespace extension returns <b>SFGAO_FILESYSTEM</b> for the item from <a href="https://msdn.microsoft.com/3864b386-7653-4661-880c-e96c08ff0dbb">IShellFolder::GetAttributesOf</a> and provides a parsing name for the item, then <b>AssocGetDetailsOfPropKey</b> will use the standard file system associations to retrieve the value for the property key.</li>
<li>If the provided namespace extension returns <b>SFGAO_FOLDER</b> | <b>SFGAO_BROWSABLE</b> for the item from <a href="https://msdn.microsoft.com/3864b386-7653-4661-880c-e96c08ff0dbb">IShellFolder::GetAttributesOf</a>, then <b>AssocGetDetailsOfPropKey</b> will use the file association for folders (<b>ASSOCCLASS_FOLDER</b>) to retrieve the value for the property key.</li>
</ol>
If the ShellFolder being implemented contains items that are extensible through the file associations mechanism, then you can use this function to retrieve <b>PropertyKeys</b> that are declared for a given file association. For example, if a given Shell folder drives a details pane and you want the properties displayed in that pane to be governed by third party file name extensions, then you can use this function to return <b>PKEY_PropList_PreviewDetails</b>.  This key has a value that is declared in the registry for that file name extension with a semicolon delimited list of properties. There is a list of file name extension defined properties in the registry. This list includes but is not limited to the following:

<ul>
<li><b>PKEY_PropList_PreviewDetails</b></li>
<li><b>PKEY_PropList_PreviewTitle</b></li>
<li><b>PKEY_PropList_FullDetails</b></li>
<li><b>PKEY_PropList_TileInfo</b></li>
<li><b>PKEY_PropList_ExtendedTileInfo</b></li>
<li><b>PKEY_PropList_InfoTip</b></li>
<li><b>PKEY_PropList_QuickTip</b></li>
<li><b>PKEY_PropList_FileOperationPrompt</b></li>
<li><b>PKEY_PropList_ConflictPrompt</b></li>
<li><b>PKEY_PropList_SetDefaultsFor</b></li>
<li><b>PKEY_PropList_NonPersonal</b></li>
<li><b>PKEY_NewMenuPreferredTypes</b></li>
<li><b>PKEY_NewMenuAllowedTypes</b></li>
</ul>


