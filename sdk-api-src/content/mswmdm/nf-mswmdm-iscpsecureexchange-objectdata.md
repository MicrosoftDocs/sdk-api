---
UID: NF:mswmdm.ISCPSecureExchange.ObjectData
title: ISCPSecureExchange::ObjectData
author: windows-sdk-content
description: The ObjectData method transfers a block of object data back to Windows Media Device Manager.
old-location: wmdm\iscpsecureexchange_objectdata.htm
old-project: WMDM
ms.assetid: 825539e4-9162-40b7-bae0-336e728fb34e
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: ISCPSecureExchange interface [windows Media Device Manager],ObjectData method, ISCPSecureExchange.ObjectData, ISCPSecureExchange::ObjectData, ISCPSecureExchangeObjectData, ObjectData, ObjectData method [windows Media Device Manager], ObjectData method [windows Media Device Manager],ISCPSecureExchange interface, mswmdm/ISCPSecureExchange::ObjectData, wmdm.iscpsecureexchange_objectdata
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mswmdm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MSVidCtlStateList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mssachlp.lib
-	mssachlp.dll
api_name:
-	ISCPSecureExchange.ObjectData
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISCPSecureExchange::ObjectData


## -description



The <b>ObjectData</b> method transfers a block of object data back to Windows Media Device Manager.




## -parameters




### -param pData [out]

Pointer to a buffer to receive data. This parameter is included in the output message authentication code and is encrypted.


### -param pdwSize [in, out]

Pointer to a <b>DWORD</b> containing the transfer size. This parameter must be included in both the input and output message authentication codes.


### -param abMac [in, out]

Array of eight bytes containing the message authentication code for the parameter data of this method. (WMDM_MAC_LENGTH is defined as 8.)


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WMDM_E_MAC_CHECK_FAILED</b></dt>
</dl>
</td>
<td width="60%">
The message authentication code is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WMDM_E_NORIGHTS</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have the rights required to perform the requested operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The method failed. Terminate interaction with the secure content provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
A parameter is an invalid or <b>NULL</b> pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>
 




## -remarks



To transfer data, Windows Media Device Manager calls the <a href="https://msdn.microsoft.com/97b55751-b45e-4204-87e2-1e653d55a718">TransferContainerData</a> method to obtain the container data. <b>ObjectData</b> is then called to transfer blocks of object data from the secure content provider to Windows Media Device Manager. If S_OK is returned with <i>pdwSize</i> set to zero, Windows Media Device Manager will request no further data.




## -see-also




<a href="https://msdn.microsoft.com/8c61e1a0-18fc-4ae9-881a-0362166012d9">ISCPSecureExchange Interface</a>
 

 

