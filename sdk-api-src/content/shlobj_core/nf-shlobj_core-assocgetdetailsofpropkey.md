---
UID: NF:shlobj_core.AssocGetDetailsOfPropKey
title: AssocGetDetailsOfPropKey function (shlobj_core.h)
description: Retrieves the value for a given property key using the file association information provided by the Namespace Extensions.
helpviewer_keywords: ["AssocGetDetailsOfPropKey","AssocGetDetailsOfPropKey function [Windows Shell]","_shell_AssocGetDetailsOfPropKey","shell.AssocGetDetailsOfPropKey","shlobj_core/AssocGetDetailsOfPropKey"]
old-location: shell\AssocGetDetailsOfPropKey.htm
tech.root: shell
ms.assetid: f13af5f4-1b6a-419c-a042-e05c9ec51d02
ms.date: 12/05/2018
ms.keywords: AssocGetDetailsOfPropKey, AssocGetDetailsOfPropKey function [Windows Shell], _shell_AssocGetDetailsOfPropKey, shell.AssocGetDetailsOfPropKey, shlobj_core/AssocGetDetailsOfPropKey
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
req.lib: 
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AssocGetDetailsOfPropKey
 - shlobj_core/AssocGetDetailsOfPropKey
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-shell-associations-l1-1-3.dll
 - api-ms-win-shell-associations-l1-1-2.dll
 - api-ms-win-shell-associations-l1-1-1.dll
 - Shell32.dll
 - API-MS-Win-Shell-Associations-L1-1-0.dll
 - Windows.Storage.dll
api_name:
 - AssocGetDetailsOfPropKey
---

# AssocGetDetailsOfPropKey function


## -description

Retrieves the value for a given property key using the file association information provided by the <a href="/windows/desktop/shell/nse-works">Namespace Extensions</a>.

## -parameters

### -param psf [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>*</b>

A pointer to the shell folder for which the details of the property key of the file association are being retrieved.

### -param pidl [in]

Type: <b>PCUITEMID_CHILD</b>

The PIDL of the child item for which the file associations are being requested.

### -param pkey [in]

Type: <b><a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a>*</b>

A pointer to the property key that is being retrieved.

### -param pv [out]

Type: <b>VARIANT*</b>

When this function returns, contains the details of the given property key.

### -param pfFoundPropKey [out]

Type: <b>BOOL*</b>

When this function returns, contains a flag that is <b>TRUE</b> if the property key was found, otherwise <b>FALSE</b>.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function is to be used only by implementers of 
     <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> <a href="/windows/desktop/shell/nse-works">Namespace Extensions</a>. Other calling applications should use 
     <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsex">IShellFolder2::GetDetailsEx</a> to get a value 
     for a <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a>. This function is to be used by 
     implementers of <b>IShellFolder</b> Namespace Extensions.

The provided namespace extension must support the use of this API in one of the following three ways.

<ol>
<li>If the provided <a href="/windows/desktop/shell/nse-works">Namespace Extensions</a> supports retrieving an <a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations">IQueryAssociations</a> interface for the item by implementing <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof">IShellFolder::GetUIObjectOf</a>(..., <b>IID_IQueryAssociations</b>, ...), then <b>AssocGetDetailsOfPropKey</b> will use the provided file associations API to retrieve the value for the property key.</li>
<li>If the provided namespace extension returns <b>SFGAO_FILESYSTEM</b> for the item from <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof">IShellFolder::GetAttributesOf</a> and provides a parsing name for the item, then <b>AssocGetDetailsOfPropKey</b> will use the standard file system associations to retrieve the value for the property key.</li>
<li>If the provided namespace extension returns <b>SFGAO_FOLDER</b> | <b>SFGAO_BROWSABLE</b> for the item from <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof">IShellFolder::GetAttributesOf</a>, then <b>AssocGetDetailsOfPropKey</b> will use the file association for folders (<b>ASSOCCLASS_FOLDER</b>) to retrieve the value for the property key.</li>
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