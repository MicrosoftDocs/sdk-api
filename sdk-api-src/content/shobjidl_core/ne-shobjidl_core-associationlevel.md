---
UID: NE:shobjidl_core.ASSOCIATIONLEVEL
title: ASSOCIATIONLEVEL (shobjidl_core.h)
description: Specifies the source of the default association for a file name extension. Used by methods of the IApplicationAssociationRegistration interface.
helpviewer_keywords: ["AL_EFFECTIVE","AL_MACHINE","AL_USER","ASSOCIATIONLEVEL","ASSOCIATIONLEVEL enumeration [Windows Shell]","_shell_ASSOCIATIONLEVEL","shell.ASSOCIATIONLEVEL","shobjidl_core/AL_EFFECTIVE","shobjidl_core/AL_MACHINE","shobjidl_core/AL_USER","shobjidl_core/ASSOCIATIONLEVEL"]
old-location: shell\ASSOCIATIONLEVEL.htm
tech.root: shell
ms.assetid: 846ce9f4-092a-420d-be73-0951efc4368f
ms.date: 12/05/2018
ms.keywords: AL_EFFECTIVE, AL_MACHINE, AL_USER, ASSOCIATIONLEVEL, ASSOCIATIONLEVEL enumeration [Windows Shell], _shell_ASSOCIATIONLEVEL, shell.ASSOCIATIONLEVEL, shobjidl_core/AL_EFFECTIVE, shobjidl_core/AL_MACHINE, shobjidl_core/AL_USER, shobjidl_core/ASSOCIATIONLEVEL
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
req.typenames: ASSOCIATIONLEVEL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ASSOCIATIONLEVEL
 - shobjidl_core/ASSOCIATIONLEVEL
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
 - ASSOCIATIONLEVEL
---

# ASSOCIATIONLEVEL enumeration


## -description

Specifies the source of the default association for a file name extension. Used by methods of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration">IApplicationAssociationRegistration</a> interface.

## -enum-fields

### -field AL_MACHINE:0

The machine-level default application association.

### -field AL_EFFECTIVE

The effective default for the current user. This value should be used by most applications.

### -field AL_USER

The per-user default application association. If this value is used and no per-user default is declared, the calling method fails with a value of <code>HRESULT_FROM_WIN32(ERROR_NO_ASSOCIATION)</code>.

## -see-also

<a href="/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a>
