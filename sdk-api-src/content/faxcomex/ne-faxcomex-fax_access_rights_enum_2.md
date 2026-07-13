---
UID: NE:faxcomex.FAX_ACCESS_RIGHTS_ENUM_2
title: FAX_ACCESS_RIGHTS_ENUM_2 (faxcomex.h)
description: Defines access rights on the fax server.
helpviewer_keywords: ["FAX_ACCESS_RIGHTS_ENUM_2","FAX_ACCESS_RIGHTS_ENUM_2 enumeration [Fax Service]","_mfax_fax_access_rights_enum_2","far2MANAGE_ARCHIVES","far2MANAGE_CONFIG","far2MANAGE_OUT_JOBS","far2MANAGE_RECEIVE_FOLDER","far2QUERY_ARCHIVES","far2QUERY_CONFIG","far2QUERY_OUT_JOBS","far2SUBMIT_HIGH","far2SUBMIT_LOW","far2SUBMIT_NORMAL","fax._mfax_fax_access_rights_enum_2","faxcomex/FAX_ACCESS_RIGHTS_ENUM_2","faxcomex/far2MANAGE_ARCHIVES","faxcomex/far2MANAGE_CONFIG","faxcomex/far2MANAGE_OUT_JOBS","faxcomex/far2MANAGE_RECEIVE_FOLDER","faxcomex/far2QUERY_ARCHIVES","faxcomex/far2QUERY_CONFIG","faxcomex/far2QUERY_OUT_JOBS","faxcomex/far2SUBMIT_HIGH","faxcomex/far2SUBMIT_LOW","faxcomex/far2SUBMIT_NORMAL"]
old-location: fax\_mfax_fax_access_rights_enum_2.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\e\faxinto_z_fax_access_rights_enum_2.htm
ms.date: 12/05/2018
ms.keywords: FAX_ACCESS_RIGHTS_ENUM_2, FAX_ACCESS_RIGHTS_ENUM_2 enumeration [Fax Service], _mfax_fax_access_rights_enum_2, far2MANAGE_ARCHIVES, far2MANAGE_CONFIG, far2MANAGE_OUT_JOBS, far2MANAGE_RECEIVE_FOLDER, far2QUERY_ARCHIVES, far2QUERY_CONFIG, far2QUERY_OUT_JOBS, far2SUBMIT_HIGH, far2SUBMIT_LOW, far2SUBMIT_NORMAL, fax._mfax_fax_access_rights_enum_2, faxcomex/FAX_ACCESS_RIGHTS_ENUM_2, faxcomex/far2MANAGE_ARCHIVES, faxcomex/far2MANAGE_CONFIG, faxcomex/far2MANAGE_OUT_JOBS, faxcomex/far2MANAGE_RECEIVE_FOLDER, faxcomex/far2QUERY_ARCHIVES, faxcomex/far2QUERY_CONFIG, faxcomex/far2QUERY_OUT_JOBS, faxcomex/far2SUBMIT_HIGH, faxcomex/far2SUBMIT_LOW, faxcomex/far2SUBMIT_NORMAL
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: FAX_ACCESS_RIGHTS_ENUM_2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FAX_ACCESS_RIGHTS_ENUM_2
 - faxcomex/FAX_ACCESS_RIGHTS_ENUM_2
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
 - FAX_ACCESS_RIGHTS_ENUM_2
---

# FAX_ACCESS_RIGHTS_ENUM_2 enumeration


## -description

Defines access rights on the fax server.

## -enum-fields

### -field far2SUBMIT_LOW:0x1

The user can submit low-priority fax jobs. Users can view and manage their jobs in the fax server's queue and their messages in the outgoing fax archive.

### -field far2SUBMIT_NORMAL:0x2

The user can submit normal-priority and low-priority fax jobs. Users can view and manage their jobs in the fax server queue and their messages in the outgoing fax archive.

### -field far2SUBMIT_HIGH:0x4

The user can submit low-priority, normal-priority, and high-priority fax jobs. Users can view and manage their jobs in the fax server queue and their messages in the outgoing fax archive.

### -field far2QUERY_OUT_JOBS:0x8

The user can query outgoing jobs belonging to all accounts, including other user's accounts.

### -field far2MANAGE_OUT_JOBS:0x10

The user can manage outgoing jobs belonging to all accounts, including other user's accounts.

### -field far2QUERY_CONFIG:0x20

The user can view and query the fax server's configuration data.

### -field far2MANAGE_CONFIG:0x40

The user can view and set the fax server's configuration data.

### -field far2QUERY_ARCHIVES:0x80

The user can query archived messages belonging to all accounts, including other user's accounts.

### -field far2MANAGE_ARCHIVES:0x100

The user can manage archived messages belonging to all accounts, including other user's accounts.

### -field far2MANAGE_RECEIVE_FOLDER:0x200

The user can manage all the messages in the server's receive folder. This includes the right to <a href="/previous-versions/windows/desktop/fax/-mfax-glossary">reassign</a> and delete messages.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxsecurity2-grantedrights-vb">IFaxSecurity2::GrantedRights</a>
