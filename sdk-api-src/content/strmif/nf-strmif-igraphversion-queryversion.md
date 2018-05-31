---
UID: NF:strmif.IGraphVersion.QueryVersion
title: IGraphVersion::QueryVersion
author: windows-sdk-content
description: The QueryVersion method retrieves the current graph version number.
old-location: dshow\igraphversion_queryversion.htm
old-project: DirectShow
ms.assetid: 297e19fd-91b5-4756-9b33-6b301c74e470
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IGraphVersion interface [DirectShow],QueryVersion method, IGraphVersion.QueryVersion, IGraphVersion::QueryVersion, IGraphVersionQueryVersion, QueryVersion, QueryVersion method [DirectShow], QueryVersion method [DirectShow],IGraphVersion interface, dshow.igraphversion_queryversion, strmif/IGraphVersion::QueryVersion
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IGraphVersion.QueryVersion
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IGraphVersion::QueryVersion


## -description



The <code>QueryVersion</code> method retrieves the current graph version number.




## -parameters




### -param pVersion

Pointer to the current graph version.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation. <b>HRESULT</b> can be one of the following standard constants, or other values not listed.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Method isn't supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK or NOERROR</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>
 




## -remarks



The version number is incremented every time there is a change in the set of filters in the graph or in their connections. If the version number has changed since the last enumeration, the graph must be re-enumerated.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/abca59f2-2134-4938-9933-bacaed771d0d">IGraphVersion Interface</a>
 

 

