---
UID: NE:shobjidl_core.ASSOCIATIONLEVEL
title: ASSOCIATIONLEVEL
author: windows-sdk-content
description: Specifies the source of the default association for a file name extension. Used by methods of the IApplicationAssociationRegistration interface.
old-location: shell\ASSOCIATIONLEVEL.htm
old-project: shell
ms.assetid: 846ce9f4-092a-420d-be73-0951efc4368f
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: AL_EFFECTIVE, AL_MACHINE, AL_USER, ASSOCIATIONLEVEL, ASSOCIATIONLEVEL enumeration [Windows Shell], _shell_ASSOCIATIONLEVEL, shell.ASSOCIATIONLEVEL, shobjidl_core/AL_EFFECTIVE, shobjidl_core/AL_MACHINE, shobjidl_core/AL_USER, shobjidl_core/ASSOCIATIONLEVEL
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: ASSOCIATIONLEVEL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - ASSOCIATIONLEVEL
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# ASSOCIATIONLEVEL enumeration


## -description


Specifies the source of the default association for a file name extension. Used by methods of the <a href="https://msdn.microsoft.com/015a3be4-2e74-4a2b-8c02-54dcbf0ecacd">IApplicationAssociationRegistration</a> interface.


## -enum-fields




### -field AL_MACHINE

The machine-level default application association.


### -field AL_EFFECTIVE

The effective default for the current user. This value should be used by most applications.


### -field AL_USER

The per-user default application association. If this value is used and no per-user default is declared, the calling method fails with a value of <code>HRESULT_FROM_WIN32(ERROR_NO_ASSOCIATION)</code>.


## -see-also




<a href="https://msdn.microsoft.com/40e6f80d-a778-4d5f-bb1b-db294815f8b5">HRESULT_FROM_WIN32</a>
 

 

