---
UID: NF:mi.MI_DestinationOptions_SetEncodePortInSPN
title: MI_DestinationOptions_SetEncodePortInSPN function
author: windows-sdk-content
description: Enables or disables the encoding of the port number in the Service Principal Name when establishing a connection to a remote machine.
old-location: wmi_v2\mi_destinationoptions_setencodeportinspn.htm
tech.root: wmi_v2
ms.assetid: cce288fe-42e0-428c-b663-931d4f5784bb
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: MI_DestinationOptions_SetEncodePortInSPN, MI_DestinationOptions_SetEncodePortInSPN function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_SetEncodePortInSPN, wmi_v2.mi_destinationoptions_setencodeportinspn
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
 - Mi.h
api_name:
 - MI_DestinationOptions_SetEncodePortInSPN
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
- apiref
: 
- 
: 
- MI_DestinationOptions_SetEncodePortInSPN
: 
---

# MI_DestinationOptions_SetEncodePortInSPN function


## -description


Enables or disables the encoding of the port number in the Service Principal Name when establishing a connection to a remote machine.


## -parameters




### -param options [in, out]

A pointer to a <a href="https://msdn.microsoft.com/7f835ff4-3917-497c-bfe9-ca335cc35938">MI_DestinationOptions</a> object returned from the <a href="https://msdn.microsoft.com/efaa1244-7fe4-4484-b9ac-e7309e2012b6">MI_Application_NewDestinationOptions</a> function.


### -param encodePort

Boolean value where <b>MI_TRUE</b> means to encode the port with SPN. <b>MI_FALSE</b> means do not.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -remarks



This function is generally used with Kerberos authentication.




## -see-also




<a href="https://msdn.microsoft.com/efaa1244-7fe4-4484-b9ac-e7309e2012b6">MI_Application_NewDestinationOptions</a>



<a href="https://msdn.microsoft.com/7f835ff4-3917-497c-bfe9-ca335cc35938">MI_DestinationOptions</a>



<a href="https://msdn.microsoft.com/aab137a0-0443-4ac0-b5b2-be6734771b73">MI_DestinationOptions_GetEncodePortInSPN</a>
 

 

