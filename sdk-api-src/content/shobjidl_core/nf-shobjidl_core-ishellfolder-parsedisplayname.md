---
UID: NF:shobjidl_core.IShellFolder.ParseDisplayName
title: IShellFolder::ParseDisplayName (shobjidl_core.h)
description: Translates the display name of a file object or a folder into an item identifier list.
helpviewer_keywords: ["IShellFolder interface [Windows Shell]","ParseDisplayName method","IShellFolder.ParseDisplayName","IShellFolder2 interface [Windows Shell]","ParseDisplayName method","IShellFolder2::ParseDisplayName","IShellFolder::ParseDisplayName","ParseDisplayName","ParseDisplayName method [Windows Shell]","ParseDisplayName method [Windows Shell]","IShellFolder interface","ParseDisplayName method [Windows Shell]","IShellFolder2 interface","_win32_IShellFolder_ParseDisplayName","shell.IShellFolder_ParseDisplayName","shobjidl_core/IShellFolder2::ParseDisplayName","shobjidl_core/IShellFolder::ParseDisplayName"]
old-location: shell\IShellFolder_ParseDisplayName.htm
tech.root: shell
ms.assetid: 099e71b0-04f2-4f82-aa00-7581bd357900
ms.date: 12/05/2018
ms.keywords: IShellFolder interface [Windows Shell],ParseDisplayName method, IShellFolder.ParseDisplayName, IShellFolder2 interface [Windows Shell],ParseDisplayName method, IShellFolder2::ParseDisplayName, IShellFolder::ParseDisplayName, ParseDisplayName, ParseDisplayName method [Windows Shell], ParseDisplayName method [Windows Shell],IShellFolder interface, ParseDisplayName method [Windows Shell],IShellFolder2 interface, _win32_IShellFolder_ParseDisplayName, shell.IShellFolder_ParseDisplayName, shobjidl_core/IShellFolder2::ParseDisplayName, shobjidl_core/IShellFolder::ParseDisplayName
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellFolder::ParseDisplayName
 - shobjidl_core/IShellFolder::ParseDisplayName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellFolder.ParseDisplayName
 - IShellFolder2.ParseDisplayName
---

# IShellFolder::ParseDisplayName


## -description

Translates the display name of a file object or a folder into an item identifier list.

## -parameters

### -param hwnd [in]

Type: <b>HWND</b>

A window handle. The client should provide a window handle if it displays a dialog or message box. Otherwise set <i>hwnd</i> to <b>NULL</b>.

### -param pbc [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a>*</b>

Optional. A pointer to a bind context used to pass parameters as inputs and outputs to the parsing function. These passed parameters are often specific to the data source and are documented by the data source owners. For example, the file system data source accepts the name being parsed (as a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa">WIN32_FIND_DATA</a> structure), using the <a href="/windows/desktop/shell/str-constants">STR_FILE_SYS_BIND_DATA</a> bind context parameter. <a href="/windows/desktop/shell/str-constants">STR_PARSE_PREFER_FOLDER_BROWSING</a> can be passed to indicate that URLs are parsed using the file system data source when possible. Construct a bind context object using <a href="/windows/desktop/api/objbase/nf-objbase-createbindctx">CreateBindCtx</a> and populate the values using <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-registerobjectparam">IBindCtx::RegisterObjectParam</a>. See <b>Bind Context String Keys</b> for a complete list of these.



If no data is being passed to or received from the parsing function, this value can be <b>NULL</b>.

### -param pszDisplayName [in]

Type: <b>LPWSTR</b>

A null-terminated Unicode string with the display name. Because each Shell folder defines its own parsing syntax, the form this string can take may vary. The desktop folder, for instance, accepts paths such as "C:\My Docs\My File.txt". It also will accept references to items in the namespace that have a GUID associated with them using the "::{GUID}" syntax. For example, to retrieve a fully qualified identifier list for the control panel from the desktop folder, you can use the following:
    
                        


```cpp
::{CLSID for Control Panel}\::{CLSID for printers folder}

```

### -param pchEaten [out]

Type: <b>ULONG*</b>

A pointer to a <b>ULONG</b> value that receives the number of characters of the display name that was parsed. If your application does not need this information, set <i>pchEaten</i> to <b>NULL</b>, and no value will be returned.

### -param ppidl [out]

Type: <b>PIDLIST_RELATIVE*</b>

When this method returns, contains a pointer to the PIDL for the object. The returned item identifier list specifies the item relative to the parsing folder. If the object associated with <i>pszDisplayName</i> is within the parsing folder, the returned item identifier list will contain only one <a href="/windows/desktop/api/shtypes/ns-shtypes-shitemid">SHITEMID</a> structure. If the object is in a subfolder of the parsing folder, the returned item identifier list will contain multiple <b>SHITEMID</b> structures. If an error occurs, <b>NULL</b> is returned in this address.
                        

When it is no longer needed, it is the responsibility of the caller to free this resource by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

### -param pdwAttributes [in, out]

Type: <b>ULONG*</b>

The value used to query for file attributes. If not used, it should be set to <b>NULL</b>. To query for one or more attributes, initialize this parameter with the <a href="/windows/desktop/shell/sfgao">SFGAO</a> flags that represent the attributes of interest. On return, those attributes that are true <i>and</i> were requested will be set.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Some Shell folders may not implement <b>IShellFolder::ParseDisplayName</b>. Each folder that does will define its own parsing syntax.

<b>ParseDisplayName</b> is not expected to handle the relative path or parent folder indicators (".\" or "..\"). It is up to the caller to remove these appropriately.

Do not use the SFGAO_VALIDATE flag in <i>pdwAttributes</i> to verify the existence of the item whose name is being parsed. <b>IShellFolder::ParseDisplayName</b> implicitly validates the existence of the item unless that behavior is overridden by a special bind context parameter.

Querying for some attributes may be relatively slow and use significant amounts of memory. For example, to determine if a file is shared, the Shell will load network components. This procedure may require the loading of several DLLs. The purpose of <i>pdwAttributes</i> is to allow you to restrict the query to only that information that is needed. The following code fragment illustrates how to find out if a file is compressed.


```cpp
LPITEMIDLIST pidl;
ULONG cbEaten;
DWORD dwAttribs = SFGAO_COMPRESSED;

hres = psf->ParseDisplayName(NULL,
                             NULL,
                             lpwszDisplayName,
                             &cbEaten,  // This can be NULL
                             &pidl,
                             &dwAttribs);

if(dwAttribs & SFGAO_COMPRESSED)
{
    // Do something with the compressed file
}

```


Since <i>pdwAttributes</i> is an in/out parameter, it should always be initialized. If you pass in an uninitialized value, some of the bits may be inadvertently set. <b>IShellFolder::ParseDisplayName</b> will then query for the corresponding attributes, which may lead to undesirable delays or memory demands. If you do not wish to query for attributes, set <i>pdwAttributes</i> to <b>NULL</b> to avoid unpredictable behavior.

This method is similar to the <a href="/windows/desktop/api/oleidl/nf-oleidl-iparsedisplayname-parsedisplayname">IParseDisplayName::ParseDisplayName</a> method.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2">IShellFolder2</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof">IShellFolder::GetAttributesOf</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka">IShellLink</a>