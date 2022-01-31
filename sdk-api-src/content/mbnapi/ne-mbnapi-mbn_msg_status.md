---
UID: NE:mbnapi.MBN_MSG_STATUS
title: MBN_MSG_STATUS (mbnapi.h)
description: The MBN_MSG_STATUS enumerated type defines the type of message being handled.
helpviewer_keywords: ["MBN_MSG_STATUS","MBN_MSG_STATUS enumeration [Microsoft Broadband Networks]","MBN_MSG_STATUS_DRAFT","MBN_MSG_STATUS_NEW","MBN_MSG_STATUS_OLD","MBN_MSG_STATUS_SENT","mbn.mbn_msg_status","mbnapi/MBN_MSG_STATUS","mbnapi/MBN_MSG_STATUS_DRAFT","mbnapi/MBN_MSG_STATUS_NEW","mbnapi/MBN_MSG_STATUS_OLD","mbnapi/MBN_MSG_STATUS_SENT"]
old-location: mbn\mbn_msg_status.htm
tech.root: mbn
ms.assetid: a63cfc67-f1bd-49b0-9a98-2d9da7fef0d2
ms.date: 12/05/2018
ms.keywords: MBN_MSG_STATUS, MBN_MSG_STATUS enumeration [Microsoft Broadband Networks], MBN_MSG_STATUS_DRAFT, MBN_MSG_STATUS_NEW, MBN_MSG_STATUS_OLD, MBN_MSG_STATUS_SENT, mbn.mbn_msg_status, mbnapi/MBN_MSG_STATUS, mbnapi/MBN_MSG_STATUS_DRAFT, mbnapi/MBN_MSG_STATUS_NEW, mbnapi/MBN_MSG_STATUS_OLD, mbnapi/MBN_MSG_STATUS_SENT
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MBN_MSG_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MBN_MSG_STATUS
 - mbnapi/MBN_MSG_STATUS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mbnapi.h
api_name:
 - MBN_MSG_STATUS
---

# MBN_MSG_STATUS enumeration


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

The <b>MBN_MSG_STATUS</b> enumerated type defines the type of message being handled.

## -enum-fields

### -field MBN_MSG_STATUS_NEW:0

The received message is newly arrived or unread.

### -field MBN_MSG_STATUS_OLD

The received message is old and read.

### -field MBN_MSG_STATUS_DRAFT

The outgoing message is unsent and stored in the device.

### -field MBN_MSG_STATUS_SENT

The outgoing message is already sent.

