---
UID: NS:mfidl._MFINPUTTRUSTAUTHORITY_ACTION
title: "_MFINPUTTRUSTAUTHORITY_ACTION"
author: windows-sdk-content
description: Describes an action requested by an output trust authority (OTA). The request is sent to an input trust authority (ITA).
old-location: mf\mfinputtrustauthority_access_action.htm
tech.root: MedFound
ms.assetid: 24e74739-054c-46ef-8df7-b29a9a2ea94a
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: 24e74739-054c-46ef-8df7-b29a9a2ea94a, MFINPUTTRUSTAUTHORITY_ACCESS_ACTION, MFINPUTTRUSTAUTHORITY_ACCESS_ACTION structure [Media Foundation], _MFINPUTTRUSTAUTHORITY_ACTION, mf.mfinputtrustauthority_access_action, mfidl/MFINPUTTRUSTAUTHORITY_ACCESS_ACTION
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - mfidl.h
api_name:
 - MFINPUTTRUSTAUTHORITY_ACCESS_ACTION
product: Windows
targetos: Windows
req.typenames: MFINPUTTRUSTAUTHORITY_ACCESS_ACTION
req.redist: 
---

# _MFINPUTTRUSTAUTHORITY_ACTION structure


## -description



Describes an action requested by an output trust authority (OTA). The request is sent to an input trust authority (ITA).




## -struct-fields




### -field Action

Specifies the action as a member of the <a href="https://msdn.microsoft.com/74cee983-e084-458b-b615-5447cca9abbc">MFPOLICYMANAGER_ACTION</a> enumeration.


### -field pbTicket

Pointer to a buffer that contains a ticket object, provided by the OTA.


### -field cbTicket

Size of the ticket object, in bytes.


## -see-also




<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

