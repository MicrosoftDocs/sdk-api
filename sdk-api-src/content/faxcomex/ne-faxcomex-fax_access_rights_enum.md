---
UID: NE:faxcomex.FAX_ACCESS_RIGHTS_ENUM
title: FAX_ACCESS_RIGHTS_ENUM (faxcomex.h)
description: The FAX_ACCESS_RIGHTS_ENUM enumeration defines access rights to the fax server.
helpviewer_keywords: ["FAX_ACCESS_RIGHTS_ENUM","FAX_ACCESS_RIGHTS_ENUM enumeration [Fax Service]","_mfax_fax_access_rights_enum","farMANAGE_CONFIG","farMANAGE_IN_ARCHIVE","farMANAGE_JOBS","farMANAGE_OUT_ARCHIVE","farQUERY_CONFIG","farQUERY_IN_ARCHIVE","farQUERY_JOBS","farQUERY_OUT_ARCHIVE","farSUBMIT_HIGH","farSUBMIT_LOW","farSUBMIT_NORMAL","fax._mfax_fax_access_rights_enum","faxcomex/FAX_ACCESS_RIGHTS_ENUM","faxcomex/farMANAGE_CONFIG","faxcomex/farMANAGE_IN_ARCHIVE","faxcomex/farMANAGE_JOBS","faxcomex/farMANAGE_OUT_ARCHIVE","faxcomex/farQUERY_CONFIG","faxcomex/farQUERY_IN_ARCHIVE","faxcomex/farQUERY_JOBS","faxcomex/farQUERY_OUT_ARCHIVE","faxcomex/farSUBMIT_HIGH","faxcomex/farSUBMIT_LOW","faxcomex/farSUBMIT_NORMAL"]
old-location: fax\_mfax_fax_access_rights_enum.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_60fh.htm
ms.date: 12/05/2018
ms.keywords: FAX_ACCESS_RIGHTS_ENUM, FAX_ACCESS_RIGHTS_ENUM enumeration [Fax Service], _mfax_fax_access_rights_enum, farMANAGE_CONFIG, farMANAGE_IN_ARCHIVE, farMANAGE_JOBS, farMANAGE_OUT_ARCHIVE, farQUERY_CONFIG, farQUERY_IN_ARCHIVE, farQUERY_JOBS, farQUERY_OUT_ARCHIVE, farSUBMIT_HIGH, farSUBMIT_LOW, farSUBMIT_NORMAL, fax._mfax_fax_access_rights_enum, faxcomex/FAX_ACCESS_RIGHTS_ENUM, faxcomex/farMANAGE_CONFIG, faxcomex/farMANAGE_IN_ARCHIVE, faxcomex/farMANAGE_JOBS, faxcomex/farMANAGE_OUT_ARCHIVE, faxcomex/farQUERY_CONFIG, faxcomex/farQUERY_IN_ARCHIVE, faxcomex/farQUERY_JOBS, faxcomex/farQUERY_OUT_ARCHIVE, faxcomex/farSUBMIT_HIGH, faxcomex/farSUBMIT_LOW, faxcomex/farSUBMIT_NORMAL
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
targetos: Windows
req.typenames: FAX_ACCESS_RIGHTS_ENUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FAX_ACCESS_RIGHTS_ENUM
 - faxcomex/FAX_ACCESS_RIGHTS_ENUM
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
 - FAX_ACCESS_RIGHTS_ENUM
---

# FAX_ACCESS_RIGHTS_ENUM enumeration


## -description

The <b>FAX_ACCESS_RIGHTS_ENUM</b> enumeration defines access rights to the fax server.

## -enum-fields

### -field farSUBMIT_LOW:0x1

The user can submit low-priority fax jobs. Users can view and manage their jobs in the fax server's queue and their messages in the outgoing fax archive.

### -field farSUBMIT_NORMAL:0x2

The user can submit normal-priority and low-priority fax jobs. Users can view and manage their jobs in the fax server queue and their messages in the outgoing fax archive.

### -field farSUBMIT_HIGH:0x4

The user can submit low-priority, normal-priority, and high-priority fax jobs. Users can view and manage their jobs in the fax server queue and their messages in the outgoing fax archive.

### -field farQUERY_JOBS:0x8

The user can view all incoming and outgoing jobs in the fax server queue.

### -field farMANAGE_JOBS:0x10

The user can manage all incoming and outgoing jobs in the fax server queue.

### -field farQUERY_CONFIG:0x20

The user can view the fax server configuration data.

### -field farMANAGE_CONFIG:0x40

The user can set the fax server configuration data.

### -field farQUERY_IN_ARCHIVE:0x80

The user can view all fax messages in the incoming archive.

### -field farMANAGE_IN_ARCHIVE:0x100

The user can manage all fax messages in the incoming archive.

### -field farQUERY_OUT_ARCHIVE:0x200

The user can view all fax messages in the outgoing archive.

### -field farMANAGE_OUT_ARCHIVE:0x400

The user can manage all fax messages in the outgoing archive.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxsecurity-grantedrights-vb">IFaxSecurity::get_GrantedRights</a>
