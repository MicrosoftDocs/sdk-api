---
UID: NF:objbase.MkParseDisplayName
title: MkParseDisplayName function (objbase.h)
description: Converts a string into a moniker that identifies the object named by the string.
helpviewer_keywords: ["MkParseDisplayName","MkParseDisplayName function [COM]","_com_MkParseDisplayName","com.mkparsedisplayname","objbase/MkParseDisplayName"]
old-location: com\mkparsedisplayname.htm
tech.root: com
ms.assetid: ada46dd3-e2c5-4ff5-89bd-3805f98b247b
ms.date: 12/05/2018
ms.keywords: MkParseDisplayName, MkParseDisplayName function [COM], _com_MkParseDisplayName, com.mkparsedisplayname, objbase/MkParseDisplayName
req.header: objbase.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MkParseDisplayName
 - objbase/MkParseDisplayName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-com-ole32-l1-4-0.dll
 - ext-ms-win-com-ole32-l1-3-0.dll
 - ext-ms-win-com-ole32-l1-2-0.dll
 - ext-ms-win-com-ole32-l1-1-5.dll
 - Ole32.dll
 - Ext-MS-Win-COM-OLE32-l1-1-1.dll
 - Ext-MS-Win-COM-OLE32-l1-1-2.dll
 - Ext-MS-Win-OLE32-IE-Ext-l1-1-0.dll
 - ext-ms-win-com-ole32-l1-1-3.dll
 - Ext-MS-Win-Com-Ole32-L1-1-4.dll
api_name:
 - MkParseDisplayName
req.apiset: ext-ms-win-com-ole32-l1-1-1 (introduced in Windows 8.1)
---

# MkParseDisplayName function


## -description

Converts a string into a moniker that identifies the object named by the string.

This function is the inverse of the <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-getdisplayname">IMoniker::GetDisplayName</a> operation, which retrieves the display name associated with a moniker.

## -parameters

### -param pbc [in]

A pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a> interface on the bind context object to be used in this binding operation.

### -param szUserName [in]

A pointer to the display name to be parsed.

### -param pchEaten [out]

A pointer to the number of characters of <i>szUserName</i> that were consumed. If the function is successful, *<i>pchEaten</i> is the length of <i>szUserName</i>; otherwise, it is the number of characters successfully parsed.

### -param ppmk [out]

The address of the <a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a>* pointer variable that receives the interface pointer to the moniker that was built from <i>szUserName</i>. When successful, the function has called <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> on the moniker and the caller is responsible for calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a>. If an error occurs, the specified interface pointer will contain as much of the moniker that the method was able to create before the error occurred.

## -returns

This function can return the standard return value E_OUTOFMEMORY, as well as the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The parse operation was successful and the moniker was created.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_E_SYNTAX</b></dt>
</dl>
</td>
<td width="60%">
Error in the syntax of a file name or an error in the syntax of the resulting composite moniker.

</td>
</tr>
</table>
 

This function can also return any of the error values returned by <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-bindtoobject">IMoniker::BindToObject</a>, <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleitemcontainer-getobject">IOleItemContainer::GetObject</a>, or <a href="/windows/desktop/api/oleidl/nf-oleidl-iparsedisplayname-parsedisplayname">IParseDisplayName::ParseDisplayName</a>.

## -remarks

The <b>MkParseDisplayName</b> function parses a human-readable name into a moniker that can be used to identify a link source. The resulting moniker can be a simple moniker (such as a file moniker), or it can be a generic composite made up of the component moniker pieces. For example, the display name "c:\mydir\somefile!item 1" 

could be parsed into the following generic composite moniker: FileMoniker based on "c:\mydir\somefile") + (ItemMoniker based on "item 1").

The most common use of <b>MkParseDisplayName</b> is in the implementation of the standard <b>Links</b> dialog box, which allows an end user to specify the source of a linked object by typing in a string. You may also need to call <b>MkParseDisplayName</b> if your application supports a macro language that permits remote references (reference to elements outside of the document). 



Parsing a display name often requires activating the same objects that would be activated during a binding operation, so it can be just as expensive (in terms of performance) as binding. Objects that are bound during the parsing operation are cached in the bind context passed to the function. If you plan to bind the moniker returned by <b>MkParseDisplayName</b>, it is best to do so immediately after the function returns, using the same bind context, which removes the need to activate objects a second time.

<b>MkParseDisplayName</b> parses as much of the display name as it understands into a moniker. The function then calls <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-parsedisplayname">IMoniker::ParseDisplayName</a> on the newly created moniker, passing the remainder of the display name. The moniker returned by <b>ParseDisplayName</b> is composed onto the end of the existing moniker and, if any of the display name remains unparsed, <b>ParseDisplayName</b> is called on the result of the composition. This process is repeated until the entire display name has been parsed.

<b>MkParseDisplayName</b> attempts the following strategies to parse the beginning of the display name, using the first one that succeeds:

<ol>
<li>
The function looks in the Running Object Table for file monikers corresponding to all prefixes of the display name that consist solely of valid file name characters. This strategy can identify documents that are as yet unsaved.

</li>
<li>
The function checks the maximal prefix of the display name, which consists solely of valid file name characters, to see if an OLE 1 document is registered by that name. In this case, the returned moniker is an internal moniker provided by the OLE 1 compatibility layer of OLE 2.

</li>
<li>
The function consults the file system to check whether a prefix of the display name matches an existing file. The file name can be drive-absolute, drive-relative, working-directory relative, or begin with an explicit network share name. This is the common case.

</li>
<li>
If the initial character of the display name is '@', the function finds the longest string immediately following it  that conforms to the legal ProgID syntax. The function converts this string to a CLSID using the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid">CLSIDFromProgID</a> function. If the CLSID represents an OLE 2 class, the function loads the corresponding class object and asks for an <a href="/windows/desktop/api/oleidl/nn-oleidl-iparsedisplayname">IParseDisplayName</a> interface pointer. The resulting <b>IParseDisplayName</b> interface is then given the whole string to parse, starting with the '@'. If the CLSID represents an OLE 1 class, then the function treats the string following the ProgID as an OLE1/DDE link designator having <i>filename</i>|<i>item</i> syntax.

</li>
</ol>

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-imoniker-getdisplayname">IMoniker::GetDisplayName</a>



<a href="/windows/desktop/api/objidl/nf-objidl-imoniker-parsedisplayname">IMoniker::ParseDisplayName</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-iparsedisplayname">IParseDisplayName</a>
