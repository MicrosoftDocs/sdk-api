---
UID: NF:bdaiface.IBDA_IPSinkControl.GetAdapterIPAddress
title: IBDA_IPSinkControl::GetAdapterIPAddress method
author: windows-driver-content
description: This interface is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems. It may be altered or unavailable in subsequent versions.
old-location: mstv\ibda_ipsinkcontrol_getadapteripaddress.htm
old-project: mstv
ms.assetid: ce9710e6-f611-4457-a282-9a7677b3055e
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetAdapterIPAddress method [Microsoft TV Technologies], GetAdapterIPAddress method [Microsoft TV Technologies], IBDA_IPSinkControl interface, GetAdapterIPAddress,IBDA_IPSinkControl.GetAdapterIPAddress, IBDA_IPSinkControl, IBDA_IPSinkControl interface [Microsoft TV Technologies], GetAdapterIPAddress method, IBDA_IPSinkControl::GetAdapterIPAddress, IBDA_IPSinkControlGetAdapterIPAddress, bdaiface/IBDA_IPSinkControl::GetAdapterIPAddress, mstv.ibda_ipsinkcontrol_getadapteripaddress
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: bdaiface.h
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
req.typenames: UICloseReasonType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	bdaiface.h
api_name:
-	IBDA_IPSinkControl.GetAdapterIPAddress
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IBDA_IPSinkControl::GetAdapterIPAddress method


## -description



This interface is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems. It may be altered or unavailable in subsequent versions.
        



The <b>GetAdapterIPAddress</b> method retrieves the IP address of the NIC.


## -parameters




### -param pulcbSize [out]

Receives the length of the buffer, in bytes.


### -param pbBuffer [out]

Pointer to a byte array containing the address.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



<b>IBDA_IPSinkControl</b> is no longer being supported for Ring 3 clients. Use the <b>BDA_IPSinkInfo</b> interface instead.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/3665c06e-0e9f-4a8a-bb72-eb0c402ce7c9">IBDA_IPSinkControl Interface</a>
 

 

