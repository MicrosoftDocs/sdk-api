---
UID: NF:faxdev.FaxDevReceive
title: FaxDevReceive function
author: windows-sdk-content
description: The fax service calls the FaxDevReceive function to signal an incoming fax transmission to the fax service provider (FSP). Each FSP must export the FaxDevReceive function.
old-location: fax\_mfax_faxdevreceive.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxfspapiref_31lx.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: FaxDevReceive, FaxDevReceive function [Fax Service], _mfax_faxdevreceive, fax._mfax_faxdevreceive, faxdev/FaxDevReceive
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: faxdev.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - UserDefined
api_location:
 - FaxDev.h
api_name:
 - FaxDevReceive
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FaxDevReceive function


## -description


The fax service calls the <b>FaxDevReceive</b> function to signal an incoming fax transmission to the fax service provider (FSP). Each FSP must export the <b>FaxDevReceive</b> function.


## -parameters




### -param FaxHandle [in]

Type: <b>HANDLE</b>

Specifies a fax handle returned by the <a href="https://msdn.microsoft.com/40f647ba-05ed-453a-8eea-729b2f59ac05">FaxDevStartJob</a> function.


### -param CallHandle [in]

Type: <b>HCALL</b>

Specifies a TAPI call handle. Note that the FSP should use this handle for all call operations, but should never close this handle. If <i>CallHandle</i> is set to <b>NULL</b>, the service requests that the FSP start receiving a fax without receiving a ring on the line. This may occur in the case when you answer the call, then realize that it's a fax call, or when you want to receive a fax during an existing call (fax polling). If the FSP does not support this option, it should return with an error. If the FSP supports this option, it should pick up the device's line and start receiving a fax.


### -param FaxReceive [in, out]

Type: <b>PFAX_RECEIVE</b>

Pointer to a <a href="https://msdn.microsoft.com/c4b14c17-13bc-4248-b51b-dca9c828bd50">FAX_RECEIVE</a> structure that contains information about an incoming fax document. Upon return, the structure also contains the <b>ReceiverName</b> and <b>ReceiverNumber</b> members.


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, the fax service calls <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The fax service calls the <b>FaxDevReceive</b> function after a TAPI line device associated with the FSP rings, and the line is in the <i>offering</i> state. For information on call states, see <a href="https://msdn.microsoft.com/a6a49b77-4e9b-4f23-bfe6-26f26549b18f">State</a> in the TAPI documentation.

The FSP must respond to the <b>FaxDevReceive</b> function by receiving the incoming fax document. The FSP must accept the incoming call through TAPI, and then receive the fax data stream. The FSP should store the data stream in the file specified by the <b>FileName</b> member of the <a href="https://msdn.microsoft.com/c4b14c17-13bc-4248-b51b-dca9c828bd50">FAX_RECEIVE</a> structure that is passed into the <b>FaxDevReceive</b> function. This file is a Tagged Image File Format Class F (TIFF Class F) file. For more information, see <a href="https://msdn.microsoft.com/d7840c10-6059-40ed-9040-50eefefc7349">Fax Image Format</a>. 

The FSP should set the <b>ReceiverName</b> and <b>ReceiverNumber</b> members in the <a href="https://msdn.microsoft.com/c4b14c17-13bc-4248-b51b-dca9c828bd50">FAX_RECEIVE</a> structure pointed to by the <i>FaxReceive</i> parameter. The fax service allocates the memory for these strings. The size of the memory the service allocates is equal to <b>sizeof(FAX_RECEIVE) + FAXDEVRECEIVE_SIZE</b>. The FSP must place the strings in the block of memory that follows the <b>FAX_RECEIVE</b> structure. The <b>ReceiverName</b> and <b>ReceiverNumber</b> members must point to the location of the strings in the memory block. For a code sample and diagram that illustrate how to fill in the memory that the fax service allocates, see <b>FAX_RECEIVE</b>.

<div class="alert"><b>Note</b>  The fax service will attempt to restore partially received faxes if the FSP reports any <a href="https://msdn.microsoft.com/b5d024c2-36f9-4f70-abab-3824f3612089">extended status</a> other than <b>FS_USER_ABORT</b>. Otherwise, the fax service will discard partially received faxes.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/c4b14c17-13bc-4248-b51b-dca9c828bd50">FAX_RECEIVE</a>



<a href="https://msdn.microsoft.com/402583fd-aef8-4197-a41e-870825c58351">Fax Service Provider Functions</a>



<a href="https://msdn.microsoft.com/9ec25812-658f-4d64-85c4-8ab66be5d93e">FaxDevSend</a>



<a href="https://msdn.microsoft.com/40f647ba-05ed-453a-8eea-729b2f59ac05">FaxDevStartJob</a>



<a href="https://msdn.microsoft.com/a8788e8a-e97c-4082-8e89-b6f4a7568d3a">Using the Fax Service Provider API</a>
 

 

