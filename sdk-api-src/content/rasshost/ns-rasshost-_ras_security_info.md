---
UID: NS:rasshost._RAS_SECURITY_INFO
title: "_RAS_SECURITY_INFO"
author: windows-sdk-content
description: The RAS_SECURITY_INFO structure is used with the RasSecurityDialogGetInfo function to return information about the RAS port associated with a RAS security DLL authentication transaction.
old-location: rras\ras_security_info_str.htm
tech.root: rras
ms.assetid: 4bf5e0b8-087c-483b-a472-eab36840f554
ms.author: windowssdkdev
ms.date: 10/23/2018
ms.keywords: "*PRAS_SECURITY_INFO, PENDING, PRAS_SECURITY_INFO, PRAS_SECURITY_INFO structure pointer [RAS], RAS_SECURITY_INFO, RAS_SECURITY_INFO structure [RAS], SUCCESS, _RAS_SECURITY_INFO, _ras_ras_security_info_str, rasshost/PRAS_SECURITY_INFO, rasshost/RAS_SECURITY_INFO, rras.ras_security_info_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: rasshost.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rasshost.h
api_name:
 - RAS_SECURITY_INFO
product: Windows
targetos: Windows
req.typenames: RAS_SECURITY_INFO, *PRAS_SECURITY_INFO
req.redist: 
---

# _RAS_SECURITY_INFO structure


## -description


The 
<b>RAS_SECURITY_INFO</b> structure is used with the 
<a href="https://msdn.microsoft.com/b7fbcfb6-686c-4464-ba78-e689019e74be">RasSecurityDialogGetInfo</a> function to return information about the RAS port associated with a RAS security DLL authentication transaction.


## -struct-fields




### -field LastError

Specifies an error code that indicates the state of the last 
<a href="https://msdn.microsoft.com/ed5fcea6-6533-4c78-bd49-dfeaafd8192a">RasSecurityDialogReceive</a> call for the port. If the receive operation failed, <b>LastError</b> is one of the error codes defined in Raserror.h or Winerror.h. Otherwise, <b>LastError</b> is one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SUCCESS"></a><a id="success"></a><dl>
<dt><b>SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The receive operation has been successfully completed. The <b>BytesReceived</b> member indicates the number of bytes received.

</td>
</tr>
<tr>
<td width="40%"><a id="PENDING"></a><a id="pending"></a><dl>
<dt><b>PENDING</b></dt>
</dl>
</td>
<td width="60%">
The receive operation is pending completion.

</td>
</tr>
</table>
 


### -field BytesReceived

Specifies the number of bytes received in the most recent 
<a href="https://msdn.microsoft.com/ed5fcea6-6533-4c78-bd49-dfeaafd8192a">RasSecurityDialogReceive</a> operation. This member is valid only if the value of the <b>LastError</b> member is SUCCESS.


### -field DeviceName

Specifies a null-terminated string that contains the user-friendly display name of the device on the port, such as Hayes SmartModem 9600.


## -see-also




<a href="https://msdn.microsoft.com/b04bef8c-a83e-4c6e-849e-feeca99699e8">RAS Server Administration Structures</a>



<a href="https://msdn.microsoft.com/b7fbcfb6-686c-4464-ba78-e689019e74be">RasSecurityDialogGetInfo</a>



<a href="https://msdn.microsoft.com/ed5fcea6-6533-4c78-bd49-dfeaafd8192a">RasSecurityDialogReceive</a>



<a href="https://msdn.microsoft.com/5016fa0b-72eb-484e-b8d7-af9de2e25689">Remote Access Service (RAS) Overview</a>
 

 

