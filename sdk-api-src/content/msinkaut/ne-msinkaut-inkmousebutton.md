---
UID: NE:msinkaut.InkMouseButton
title: InkMouseButton (msinkaut.h)
description: Specifies which mouse button was pressed.
helpviewer_keywords: ["38db0d8e-a6db-42fa-8269-69254d38cba8","IMF_Left","IMF_Middle","IMF_Right","InkMouseButton","InkMouseButton enumeration [Tablet PC]","msinkaut/IMF_Left","msinkaut/IMF_Middle","msinkaut/IMF_Right","msinkaut/InkMouseButton","tablet.inkmousebutton"]
old-location: tablet\inkmousebutton.htm
tech.root: tablet
ms.assetid: 38db0d8e-a6db-42fa-8269-69254d38cba8
ms.date: 12/05/2018
ms.keywords: 38db0d8e-a6db-42fa-8269-69254d38cba8, IMF_Left, IMF_Middle, IMF_Right, InkMouseButton, InkMouseButton enumeration [Tablet PC], msinkaut/IMF_Left, msinkaut/IMF_Middle, msinkaut/IMF_Right, msinkaut/InkMouseButton, tablet.inkmousebutton
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: InkMouseButton
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InkMouseButton
 - msinkaut/InkMouseButton
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - msinkaut.h
api_name:
 - InkMouseButton
---

# InkMouseButton enumeration


## -description

Specifies which mouse button was pressed.

## -enum-fields

### -field IMF_Left:1

The left mouse button was pressed.

### -field IMF_Right:2

The right mouse button was pressed.

### -field IMF_Middle:4

The middle mouse button was pressed.

## -remarks

In C++, explicit casting is required when trying to set more than one flag at a time. A compilation error occurs if explicit casting is not used.

## -see-also

<a href="/windows/desktop/tablet/inkpicture-mousedown">MouseDown Event [InkPicture Control]</a>



<a href="/windows/desktop/tablet/inkpicture-mousemove">MouseMove Event [InkPicture Control]</a>



<a href="/windows/desktop/tablet/inkpicture-mouseup">MouseUp Event [InkPicture Control]</a>



<a href="/windows/desktop/tablet/inkpicture-mousewheel">MouseWheel Event [InkPicture Control]</a>
