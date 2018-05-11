---
UID: NF:wmsdkidl.WMCreateWriter
title: WMCreateWriter function
author: windows-driver-content
description: The WMCreateWriter function creates a writer object.
old-location: wmformat\wmcreatewriter.htm
old-project: wmformat
ms.assetid: 26d42213-40a1-4e2c-805b-c0803ee015b4
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: WMCreateWriter, WMCreateWriter function [windows Media Format], wmformat.wmcreatewriter, wmsdkidl/WMCreateWriter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
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
req.typenames: WM_AETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wmvcore.dll
api_name:
-	WMCreateWriter
product: Windows
targetos: Windows
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WMCreateWriter function


## -description



The <b>WMCreateWriter</b> function creates a writer object.




## -parameters




### -param pUnkCert

TBD


### -param ppWriter [out]

Pointer to a pointer to the <a href="https://msdn.microsoft.com/a194ef11-5203-4e85-af91-cdce0c53fe76">IWMWriter</a> interface of the newly created writer object.


#### - pUnkReserved [in]

Pointer to an <b>IUnknown</b> interface. This value is not used and should be set to <b>NULL</b>.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The function succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The function is unable to allocate memory for the new object.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/8058b7fe-7d02-4572-ad43-6867d4ceb7e9">Writer Object</a>
 

 

