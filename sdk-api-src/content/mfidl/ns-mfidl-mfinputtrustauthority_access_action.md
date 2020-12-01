---
UID: NS:mfidl._MFINPUTTRUSTAUTHORITY_ACTION
title: MFINPUTTRUSTAUTHORITY_ACCESS_ACTION (mfidl.h)
description: Describes an action requested by an output trust authority (OTA). The request is sent to an input trust authority (ITA).
helpviewer_keywords: ["24e74739-054c-46ef-8df7-b29a9a2ea94a","MFINPUTTRUSTAUTHORITY_ACCESS_ACTION","MFINPUTTRUSTAUTHORITY_ACCESS_ACTION structure [Media Foundation]","mf.mfinputtrustauthority_access_action","mfidl/MFINPUTTRUSTAUTHORITY_ACCESS_ACTION"]
old-location: mf\mfinputtrustauthority_access_action.htm
tech.root: mf
ms.assetid: 24e74739-054c-46ef-8df7-b29a9a2ea94a
ms.date: 12/05/2018
ms.keywords: 24e74739-054c-46ef-8df7-b29a9a2ea94a, MFINPUTTRUSTAUTHORITY_ACCESS_ACTION, MFINPUTTRUSTAUTHORITY_ACCESS_ACTION structure [Media Foundation], mf.mfinputtrustauthority_access_action, mfidl/MFINPUTTRUSTAUTHORITY_ACCESS_ACTION
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
targetos: Windows
req.typenames: MFINPUTTRUSTAUTHORITY_ACCESS_ACTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFINPUTTRUSTAUTHORITY_ACTION
 - mfidl/_MFINPUTTRUSTAUTHORITY_ACTION
 - MFINPUTTRUSTAUTHORITY_ACCESS_ACTION
 - mfidl/MFINPUTTRUSTAUTHORITY_ACCESS_ACTION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MFINPUTTRUSTAUTHORITY_ACCESS_ACTION
---

# MFINPUTTRUSTAUTHORITY_ACCESS_ACTION structure


## -description

Describes an action requested by an output trust authority (OTA). The request is sent to an input trust authority (ITA).

## -struct-fields

### -field Action

Specifies the action as a member of the <a href="/windows/desktop/api/mfidl/ne-mfidl-mfpolicymanager_action">MFPOLICYMANAGER_ACTION</a> enumeration.

### -field pbTicket

Pointer to a buffer that contains a ticket object, provided by the OTA.

### -field cbTicket

Size of the ticket object, in bytes.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>