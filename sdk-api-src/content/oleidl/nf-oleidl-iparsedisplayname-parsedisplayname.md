---
UID: NF:oleidl.IParseDisplayName.ParseDisplayName
title: IParseDisplayName::ParseDisplayName
author: windows-sdk-content
description: Parses the specified display name and creates a corresponding moniker.
old-location: com\iparsedisplayname_parsedisplayname.htm
tech.root: com
ms.assetid: bf18320c-1ff3-4280-bd67-70f6c2998285
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IParseDisplayName interface [COM],ParseDisplayName method, IParseDisplayName.ParseDisplayName, IParseDisplayName::ParseDisplayName, ParseDisplayName, ParseDisplayName method [COM], ParseDisplayName method [COM],IParseDisplayName interface, _com_iparsedisplayname_parsedisplayname, com.iparsedisplayname_parsedisplayname, oleidl/IParseDisplayName::ParseDisplayName
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IParseDisplayName.ParseDisplayName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IParseDisplayName::ParseDisplayName


## -description


Parses the specified display name and creates a corresponding moniker.


## -parameters




### -param pbc [in]

A pointer to the bind context to be used in this binding operation. See <a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a>.


### -param pszDisplayName [in]

The display name to be parsed.


### -param pchEaten [out]

A pointer to a variable that receives the number of characters in the display name that correspond to the <i>ppmkOut</i> moniker.


### -param ppmkOut [out]

A pointer to an <a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a> pointer variable that receives the interface pointer to the resulting moniker. If an error occurs, the implementation sets *<i>ppmkOut</i> to <b>NULL</b>. If *<i>ppmkOut</i> is non-<b>NULL</b>, the implementation must call <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a>; it is the caller's responsibility to call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a>.


## -returns



This method can return the standard return values E_OUTOFMEMORY and E_UNEXPECTED, as well as the following values.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_E_SYNTAX</b></dt>
</dl>
</td>
<td width="60%">
There is a syntax error in the display name. Parsing failed because <i>pszDisplayName</i> could only be partially resolved into a moniker. In this case, *<i>pchEaten</i> has the number of characters that were successfully parsed into a moniker prefix. The parameter <i>ppmkOut</i> should be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_E_NOOBJECT</b></dt>
</dl>
</td>
<td width="60%">
The display name does not identify a component in this namespace.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are not valid.

</td>
</tr>
</table>
 




## -remarks



In general, the maximum prefix of <i>pszDisplayName</i> that is syntactically valid and that represents an object should be consumed by this method and converted to a moniker.

Typically, this method is called by <a href="https://msdn.microsoft.com/ada46dd3-e2c5-4ff5-89bd-3805f98b247b">MkParseDisplayName</a> or <a href="https://msdn.microsoft.com/library/ms775113(v=VS.85).aspx">MkParseDisplayNameEx</a>. In the initial step of the parsing operation, these functions can retrieve the <a href="https://msdn.microsoft.com/37844d9b-35ce-4d30-8a58-dac4c671896f">IParseDisplayName</a> interface directly from an instance of a class identified with either the "@ProgID" or "ProgID" notation. Subsequent parsing steps can query for the interface on an intermediate object.

The main loops of <a href="https://msdn.microsoft.com/ada46dd3-e2c5-4ff5-89bd-3805f98b247b">MkParseDisplayName</a> and <a href="https://msdn.microsoft.com/library/ms775113(v=VS.85).aspx">MkParseDisplayNameEx</a> find the next moniker piece by calling the equivalent method in the <a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a> interface, that is, <a href="https://msdn.microsoft.com/6a5a1f14-f14f-404b-90d8-0afceafc087c">IMoniker::ParseDisplayName</a>, on the moniker that it currently holds. In this call to <b>IMoniker::ParseDisplayName</b>, the <b>MkParseDisplayName</b> or <b>MkParseDisplayNameEx</b> function passes <b>NULL</b> in the <i>pmkToLeft</i> parameter. If the moniker currently held is a generic composite, the call to <b>IMoniker::ParseDisplayName</b> is forwarded by that composite onto its last piece, passing the prefix of the composite to the left of the piece in <i>pmkToLeft</i>.

Some moniker classes will be able to handle this parsing internally to themselves because they are designed to designate only certain kinds of objects. Others will need to bind to the object that they designate to accomplish the parsing process. As is usual, these objects should not be released by <a href="https://msdn.microsoft.com/6a5a1f14-f14f-404b-90d8-0afceafc087c">IMoniker::ParseDisplayName</a> but instead should be transferred to the bind context via <a href="https://msdn.microsoft.com/84d49231-5fdd-4a89-8e76-1f0e56bc553f">IBindCtx::RegisterObjectBound</a> or <a href="https://msdn.microsoft.com/26938d07-d772-4e72-a6aa-57dd2f2cece1">IBindCtx::GetRunningObjectTable</a> followed by <a href="https://msdn.microsoft.com/40f815b2-dfea-416c-aae1-7ba3a710ad91">IRunningObjectTable::Register</a> for release at a later time.




## -see-also




<a href="https://msdn.microsoft.com/6a5a1f14-f14f-404b-90d8-0afceafc087c">IMoniker::ParseDisplayName</a>



<a href="https://msdn.microsoft.com/37844d9b-35ce-4d30-8a58-dac4c671896f">IParseDisplayName</a>



<a href="https://msdn.microsoft.com/ada46dd3-e2c5-4ff5-89bd-3805f98b247b">MkParseDisplayName</a>



<a href="https://msdn.microsoft.com/library/ms775113(v=VS.85).aspx">MkParseDisplayNameEx</a>
 

 

