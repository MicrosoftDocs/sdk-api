---
UID: NF:bits.IBackgroundCopyError.GetProtocol
title: IBackgroundCopyError::GetProtocol
author: windows-sdk-content
description: Retrieves the protocol used to transfer the file. The remote file name identifies the protocol to use to transfer the file.
old-location: bits\ibackgroundcopyerror_getprotocol.htm
tech.root: bits
ms.assetid: 94c1fcc8-7132-41db-9a1c-cbe105e3b0bb
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetProtocol, GetProtocol method [BITS], GetProtocol method [BITS],IBackgroundCopyError interface, IBackgroundCopyError interface [BITS],GetProtocol method, IBackgroundCopyError.GetProtocol, IBackgroundCopyError::GetProtocol, _drz_ibackgroundcopyerror_getprotocol, bits.ibackgroundcopyerror_getprotocol, bits/IBackgroundCopyError::GetProtocol
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: bits.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: QmgrPrxy.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - QmgrPrxy.dll
api_name:
 - IBackgroundCopyError.GetProtocol
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBackgroundCopyError::GetProtocol


## -description


Retrieves the protocol used to transfer the file. The remote file name identifies the protocol to use to transfer the file.


## -parameters




### -param pProtocol [out]

Null-terminated string that contains the protocol used to transfer the file. The string contains "http" for the HTTP protocol and "file" for the SMB protocol. The <i>ppProtocol</i> parameter is set to <b>NULL</b> if the error is not related to the transfer protocol. Call the 
<a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> function to free <i>ppProtocol</i> when done.


## -returns



This method returns the following <b>HRESULT</b> values, as well as others.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
Successfully retrieved the remote file protocol.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_PROTOCOL_NOT_AVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The error is not associated with the remote file transfer protocol. The <i>ppProtocol</i> parameter is set to <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/a0b9e887-84d5-4f67-a65c-6a807c50dafd">IBackgroundCopyError</a>
 

 

