---
UID: NF:encdec.IDTFilter2.GetLastErrorCode
title: IDTFilter2::GetLastErrorCode
author: windows-sdk-content
description: The GetLastErrorCode method returns the most recent error code from the Decrypter/Detagger filter.
old-location: mstv\idtfilter2_getlasterrorcode.htm
tech.root: MSTV
ms.assetid: e4de424c-0db6-408e-ab1a-57ae8899f4a7
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetLastErrorCode, GetLastErrorCode method [Microsoft TV Technologies], GetLastErrorCode method [Microsoft TV Technologies],IDTFilter2 interface, IDTFilter2 interface [Microsoft TV Technologies],GetLastErrorCode method, IDTFilter2.GetLastErrorCode, IDTFilter2::GetLastErrorCode, IDTFilter2GetLastErrorCode, encdec/IDTFilter2::GetLastErrorCode, mstv.idtfilter2_getlasterrorcode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: encdec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: None supported
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - EncDec.h
api_name:
 - IDTFilter2.GetLastErrorCode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDTFilter2::GetLastErrorCode


## -description


The <b>GetLastErrorCode</b> method returns the most recent error code from the Decrypter/Detagger filter.


## -parameters






## -returns



Returns an <b>HRESULT</b>. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_DRM_APPCERT_REVOKED</b></dt>
</dl>
</td>
<td width="60%">
A problem has occurred in the digital rights management (DRM) component.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_DRM_CERTIFICATE_REVOKED</b></dt>
</dl>
</td>
<td width="60%">
The client's certificate has been revoked.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
No DRM errors have occurred.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/15acf764-7e4d-40c3-b907-ff5dfaa69dae">IDTFilter Interface</a>
 

 

