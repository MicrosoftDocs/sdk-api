---
UID: NE:faxcomex.FAX_SERVER_APIVERSION_ENUM
title: FAX_SERVER_APIVERSION_ENUM (faxcomex.h)
description: The FAX_SERVER_APIVERSION_ENUM enumeration defines the version of the fax API. No value below is supported on any version of the fax service earlier than the one it designates.
helpviewer_keywords: ["FAX_SERVER_APIVERSION_ENUM","FAX_SERVER_APIVERSION_ENUM enumeration [Fax Service]","_mfax_fax_server_apiversion_enum","fax._mfax_fax_server_apiversion_enum","faxcomex/FAX_SERVER_APIVERSION_ENUM","faxcomex/fsAPI_VERSION_0","faxcomex/fsAPI_VERSION_1","faxcomex/fsAPI_VERSION_2","faxcomex/fsAPI_VERSION_3","fsAPI_VERSION_0","fsAPI_VERSION_1","fsAPI_VERSION_2","fsAPI_VERSION_3"]
old-location: fax\_mfax_fax_server_apiversion_enum.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_0pbh.htm
ms.date: 12/05/2018
ms.keywords: FAX_SERVER_APIVERSION_ENUM, FAX_SERVER_APIVERSION_ENUM enumeration [Fax Service], _mfax_fax_server_apiversion_enum, fax._mfax_fax_server_apiversion_enum, faxcomex/FAX_SERVER_APIVERSION_ENUM, faxcomex/fsAPI_VERSION_0, faxcomex/fsAPI_VERSION_1, faxcomex/fsAPI_VERSION_2, faxcomex/fsAPI_VERSION_3, fsAPI_VERSION_0, fsAPI_VERSION_1, fsAPI_VERSION_2, fsAPI_VERSION_3
req.header: faxcomex.h
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
targetos: Windows
req.typenames: FAX_SERVER_APIVERSION_ENUM
req.redist: the value used)
ms.custom: 19H1
f1_keywords:
 - FAX_SERVER_APIVERSION_ENUM
 - faxcomex/FAX_SERVER_APIVERSION_ENUM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FaxComex.h
api_name:
 - FAX_SERVER_APIVERSION_ENUM
---

# FAX_SERVER_APIVERSION_ENUM enumeration


## -description

The <b>FAX_SERVER_APIVERSION_ENUM </b> enumeration defines the version of the fax API. No value below is supported on any version of the fax service earlier than the one it designates.

## -enum-fields

### -field fsAPI_VERSION_0:0

API Version 0, the fax service API used by the BackOffice Small Business Server 2000 (SBS) and BackOffice Server 2000 (BOS). Not supported.

### -field fsAPI_VERSION_1:0x10000

API Version 1, the fax service API used by the Windows XP fax service server.

### -field fsAPI_VERSION_2:0x20000

API Version 2, the fax service API used by the Windows Server 2003 fax service server.

### -field fsAPI_VERSION_3:0x30000

API Version 3, the fax service API used by the Windows Vista fax service server.

