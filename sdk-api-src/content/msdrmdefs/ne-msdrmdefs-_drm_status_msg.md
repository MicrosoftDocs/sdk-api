---
UID: NE:msdrmdefs._DRM_STATUS_MSG
title: "_DRM_STATUS_MSG"
author: windows-sdk-content
description: Used by the custom callback function to specify why the callback function is being called.
old-location: rm\drm_status_msg.htm
old-project: adrms_sdk
ms.assetid: 9420c415-09ef-43a0-b458-bfaae9857314
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DRM_MSG_ACQUIRE_ADVISORY, DRM_MSG_ACQUIRE_CLIENTLICENSOR, DRM_MSG_ACQUIRE_ISSUANCE_LICENSE_TEMPLATE, DRM_MSG_ACQUIRE_LICENSE, DRM_MSG_ACTIVATE_GROUPIDENTITY, DRM_MSG_ACTIVATE_MACHINE, DRM_MSG_SIGN_ISSUANCE_LICENSE, DRM_STATUS_MSG, DRM_STATUS_MSG enumeration [Active Directory Rights Management Services SDK 1.0], _DRM_STATUS_MSG, msdrmdefs/DRM_MSG_ACQUIRE_ADVISORY, msdrmdefs/DRM_MSG_ACQUIRE_CLIENTLICENSOR, msdrmdefs/DRM_MSG_ACQUIRE_ISSUANCE_LICENSE_TEMPLATE, msdrmdefs/DRM_MSG_ACQUIRE_LICENSE, msdrmdefs/DRM_MSG_ACTIVATE_GROUPIDENTITY, msdrmdefs/DRM_MSG_ACTIVATE_MACHINE, msdrmdefs/DRM_MSG_SIGN_ISSUANCE_LICENSE, msdrmdefs/DRM_STATUS_MSG, rm.drm_status_msg
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: msdrmdefs.h
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
tech.root: 
req.typenames: DRM_STATUS_MSG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Msdrmdefs.h
api_name:
 - DRM_STATUS_MSG
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# _DRM_STATUS_MSG enumeration


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRM_STATUS_MSG</b> enumeration is used by the custom callback function to specify why the callback function is being called.


## -enum-fields




### -field DRM_MSG_ACTIVATE_MACHINE

AD RMS is attempting to activate the machine. For more information, see the <a href="https://msdn.microsoft.com/1006464b-5fd2-4bc0-ac43-aacc5cd02322">DRM_MSG_ACTIVATE_MACHINE</a> message.


### -field DRM_MSG_ACTIVATE_GROUPIDENTITY

AD RMS is attempting to activate a user. For more information, see the <a href="https://msdn.microsoft.com/49c8606a-c2d9-4380-9b99-139d75b0689b">DRM_MSG_ACTIVATE_GROUPIDENTITY</a> message.


### -field DRM_MSG_ACQUIRE_LICENSE

AD RMS is attempting to acquire a license. For more information, see the <a href="https://msdn.microsoft.com/df1635f1-3be3-4043-9ad9-afb29e24986a">DRM_MSG_ACQUIRE_LICENSE</a> message.


### -field DRM_MSG_ACQUIRE_ADVISORY

AD RMS is attempting to acquire a revocation list. For more information, see the <a href="https://msdn.microsoft.com/9984503c-9670-4ab1-acdb-460f420ee4e6">DRM_MSG_ACQUIRE_ADVISORY</a> message.


### -field DRM_MSG_SIGN_ISSUANCE_LICENSE

AD RMS is attempting to acquire a signed issuance license. For more information, see the <a href="https://msdn.microsoft.com/0d61bd67-74d7-4c13-834d-94154ac9b527">DRM_MSG_SIGN_ISSUANCE_LICENSE</a> message.


### -field DRM_MSG_ACQUIRE_CLIENTLICENSOR

AD RMS is attempting to acquire a client licensor certificate. For more information, see the <a href="https://msdn.microsoft.com/a4ead9c1-eda6-4af8-9831-9870a73d8e81">DRM_MSG_ACQUIRE_CLIENTLICENSOR</a> message.


### -field DRM_MSG_ACQUIRE_ISSUANCE_LICENSE_TEMPLATE

AD RMS is attempting to acquire a template collection. For more information, see the <a href="https://msdn.microsoft.com/e690fd96-c11f-43fe-85ad-466f62209e6d">DRM_MSG_ACQUIRE_ISSUANCE_LICENSE_TEMPLATE</a> message.


## -remarks



The callback function can use this message, together with the <i>hr</i> parameter, to determine the status of a request to a server.




## -see-also




<a href="https://msdn.microsoft.com/bc3a8ab3-9f89-442b-9910-85820b2b2653">AD RMS Enumerations</a>



<a href="https://msdn.microsoft.com/7d880b74-1934-4282-a7ca-1dac3602d6b4">Creating a Callback Function</a>



<a href="https://msdn.microsoft.com/42c58096-429c-4278-b9ab-8c5a91361af8">DRMAcquireAdvisories</a>



<a href="https://msdn.microsoft.com/0d4ce794-8384-4f1c-bc8c-1e67fbb5f987">DRMAcquireLicense</a>



<a href="https://msdn.microsoft.com/d3f4ac2c-95d9-4273-a679-81670dd62d28">DRMActivate</a>
 

 

