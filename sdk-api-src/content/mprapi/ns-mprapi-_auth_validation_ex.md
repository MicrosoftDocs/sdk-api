---
UID: NS:mprapi._AUTH_VALIDATION_EX
title: "_AUTH_VALIDATION_EX"
author: windows-sdk-content
description: Used for enabling clients to bypass Point-to-Point (PPP) authentication during Secure Socket Tunneling Protocol (SSTP) connection establishment.
old-location: rras\auth_validation_ex.htm
tech.root: rras
ms.assetid: 17e78379-a9f8-4aab-aff3-aa9b21eb629c
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: AUTH_VALIDATION_EX, AUTH_VALIDATION_EX structure [RAS], PAUTH_VALIDATION_EX, PAUTH_VALIDATION_EX structure pointer [RAS], _AUTH_VALIDATION_EX, mprapi/AUTH_VALIDATION_EX, mprapi/PAUTH_VALIDATION_EX, rras.auth_validation_ex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - Mprapi.h
api_name:
 - AUTH_VALIDATION_EX
product: Windows
targetos: Windows
req.typenames: AUTH_VALIDATION_EX
req.redist: 
---

# _AUTH_VALIDATION_EX structure


## -description


The <b>AUTH_VALIDATION_EX</b> structure is used for enabling clients to  bypass Point-to-Point (PPP) authentication during Secure Socket Tunneling Protocol (SSTP) connection establishment.


## -struct-fields




### -field Header

A <a href="https://msdn.microsoft.com/2f4e1ddc-7991-4091-9889-fdd2d75e702f">MPRAPI_OBJECT_HEADER</a> structure that specifies the version of the <b>AUTH_VALIDATION_EX</b> structure. 

<div class="alert"><b>Note</b>  The <b>revision</b> member  of  <b>Header</b> must be <b>0x01</b> and <b>type</b> must be <b>MPRAPI_OBJECT_TYPE_AUTH_VALIDATION_OBJECT</b>.</div>
<div> </div>

### -field hRasConnection

A handle to the RAS connection for which PPP authentication is being bypassed. This can be a handle returned by the 
<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a> or 
<a href="https://msdn.microsoft.com/b581cfbf-a55e-4f56-89cd-168aa23af550">RasEnumConnections</a> function.


### -field wszUserName

A null-terminated Unicode string that contains the name of the user logging on to the connection.


### -field wszLogonDomain

A null-terminated Unicode string that contains the domain on which the connected user is authenticating.


### -field AuthInfoSize

The size, in bytes, of the user authentication information in <b>AuthInfo</b>.


### -field AuthInfo

A <b>BYTE</b> array that contains the user authentication information required to bypass PPP authentication during SSTP connection negotiation.


## -see-also




<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>



<a href="https://msdn.microsoft.com/767733eb-1cbd-4b8d-98b7-41d1d0f2c630">Router Management Structures</a>
 

 

