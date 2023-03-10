---
UID: NE:shobjidl_core.ASSOCIATIONTYPE
title: ASSOCIATIONTYPE (shobjidl_core.h)
description: Specifies the type of association for an application. Used by methods of the IApplicationAssociationRegistration interface.
helpviewer_keywords: ["ASSOCIATIONTYPE","ASSOCIATIONTYPE enumeration [Windows Shell]","AT_FILEEXTENSION","AT_MIMETYPE","AT_STARTMENUCLIENT","AT_URLPROTOCOL","_shell_ASSOCIATIONTYPE","shell.ASSOCIATIONTYPE","shobjidl_core/ASSOCIATIONTYPE","shobjidl_core/AT_FILEEXTENSION","shobjidl_core/AT_MIMETYPE","shobjidl_core/AT_STARTMENUCLIENT","shobjidl_core/AT_URLPROTOCOL"]
old-location: shell\ASSOCIATIONTYPE.htm
tech.root: shell
ms.assetid: 3dbbe748-5e83-4103-932a-b51a2a55f9fd
ms.date: 12/05/2018
ms.keywords: ASSOCIATIONTYPE, ASSOCIATIONTYPE enumeration [Windows Shell], AT_FILEEXTENSION, AT_MIMETYPE, AT_STARTMENUCLIENT, AT_URLPROTOCOL, _shell_ASSOCIATIONTYPE, shell.ASSOCIATIONTYPE, shobjidl_core/ASSOCIATIONTYPE, shobjidl_core/AT_FILEEXTENSION, shobjidl_core/AT_MIMETYPE, shobjidl_core/AT_STARTMENUCLIENT, shobjidl_core/AT_URLPROTOCOL
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ASSOCIATIONTYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ASSOCIATIONTYPE
 - shobjidl_core/ASSOCIATIONTYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - ASSOCIATIONTYPE
---

# ASSOCIATIONTYPE enumeration


## -description

Specifies the type of association for an application. Used by methods of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration">IApplicationAssociationRegistration</a> interface.

## -enum-fields

### -field AT_FILEEXTENSION:0

Indicates a file name extension, such as <code>.htm</code> or <code>.mp3</code>.

### -field AT_URLPROTOCOL

Indicates a protocol, such as <code>http</code> or <code>mailto</code>.

### -field AT_STARTMENUCLIENT

Indicates the owner of the startmenu client for a mail or Internet hyperlink. As of Windows 7, this value is used only for the MAPI sendmail client.

### -field AT_MIMETYPE

Indicates the MIME type, such as <code>audio/mp3</code>.
