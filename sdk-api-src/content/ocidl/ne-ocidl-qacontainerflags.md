---
UID: NE:ocidl.tagQACONTAINERFLAGS
title: QACONTAINERFLAGS (ocidl.h)
description: Indicates ambient properties supplied by the container. It is used in the dwAmbientFlags member of the QACONTAINER structure.
helpviewer_keywords: ["QACONTAINERFLAGS","QACONTAINERFLAGS enumeration [COM]","QACONTAINER_AUTOCLIP","QACONTAINER_DISPLAYASDEFAULT","QACONTAINER_MESSAGEREFLECT","QACONTAINER_SHOWGRABHANDLES","QACONTAINER_SHOWHATCHING","QACONTAINER_SUPPORTSMNEMONICS","QACONTAINER_UIDEAD","QACONTAINER_USERMODE","_ctrl_QACONTAINERFLAGS","com.qacontainerflags","ocidl/QACONTAINERFLAGS","ocidl/QACONTAINER_AUTOCLIP","ocidl/QACONTAINER_DISPLAYASDEFAULT","ocidl/QACONTAINER_MESSAGEREFLECT","ocidl/QACONTAINER_SHOWGRABHANDLES","ocidl/QACONTAINER_SHOWHATCHING","ocidl/QACONTAINER_SUPPORTSMNEMONICS","ocidl/QACONTAINER_UIDEAD","ocidl/QACONTAINER_USERMODE"]
old-location: com\qacontainerflags.htm
tech.root: com
ms.assetid: bcca4762-7c4b-4062-8d41-6b2027045886
ms.date: 12/05/2018
ms.keywords: QACONTAINERFLAGS, QACONTAINERFLAGS enumeration [COM], QACONTAINER_AUTOCLIP, QACONTAINER_DISPLAYASDEFAULT, QACONTAINER_MESSAGEREFLECT, QACONTAINER_SHOWGRABHANDLES, QACONTAINER_SHOWHATCHING, QACONTAINER_SUPPORTSMNEMONICS, QACONTAINER_UIDEAD, QACONTAINER_USERMODE, _ctrl_QACONTAINERFLAGS, com.qacontainerflags, ocidl/QACONTAINERFLAGS, ocidl/QACONTAINER_AUTOCLIP, ocidl/QACONTAINER_DISPLAYASDEFAULT, ocidl/QACONTAINER_MESSAGEREFLECT, ocidl/QACONTAINER_SHOWGRABHANDLES, ocidl/QACONTAINER_SHOWHATCHING, ocidl/QACONTAINER_SUPPORTSMNEMONICS, ocidl/QACONTAINER_UIDEAD, ocidl/QACONTAINER_USERMODE
req.header: ocidl.h
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
req.typenames: QACONTAINERFLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagQACONTAINERFLAGS
 - ocidl/tagQACONTAINERFLAGS
 - QACONTAINERFLAGS
 - ocidl/QACONTAINERFLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OCIdl.h
api_name:
 - QACONTAINERFLAGS
---

# QACONTAINERFLAGS enumeration


## -description

Indicates ambient properties supplied by the container. It is used in the <b>dwAmbientFlags</b> member of the <a href="/windows/desktop/api/ocidl/ns-ocidl-qacontainer">QACONTAINER</a> structure.

## -enum-fields

### -field QACONTAINER_SHOWHATCHING:0x1

Specifies the ShowHatching ambient property, which has a standard ambient DISPID of -712.

### -field QACONTAINER_SHOWGRABHANDLES:0x2

Specifies the ShowGrabHandles ambient property, which has a standard ambient DISPID of -711.

### -field QACONTAINER_USERMODE:0x4

Specifies the UserMode ambient property, which has a standard ambient DISPID of -709.

### -field QACONTAINER_DISPLAYASDEFAULT:0x8

Specifies the DisplayAsDefault ambient property, which has a standard ambient DISPID of -713.

### -field QACONTAINER_UIDEAD:0x10

Specifies the UIDead ambient property, which has a standard ambient DISPID of -710.

### -field QACONTAINER_AUTOCLIP:0x20

Specifies the AutoClip ambient property, which has a standard ambient DISPID of -715.

### -field QACONTAINER_MESSAGEREFLECT:0x40

Specifies the MessageReflect ambient property, which has a standard ambient DISPID of -706.

### -field QACONTAINER_SUPPORTSMNEMONICS:0x80

Specifies the SupportsMnemonics ambient property, which has a standard ambient DISPID of -714.

## -see-also

<a href="/windows/desktop/api/ocidl/ns-ocidl-qacontainer">QACONTAINER</a>
