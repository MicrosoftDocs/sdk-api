---
UID: NE:msinkaut.InkMousePointer
title: InkMousePointer (msinkaut.h)
description: Specifies the type of mouse pointer to appear.
helpviewer_keywords: ["74f489f2-d568-4133-96e6-de15cbfabfe7","IMP_Arrow","IMP_ArrowHourglass","IMP_ArrowQuestion","IMP_Crosshair","IMP_Custom","IMP_Default","IMP_Hand","IMP_Hourglass","IMP_Ibeam","IMP_NoDrop","IMP_SizeAll","IMP_SizeNESW","IMP_SizeNS","IMP_SizeNWSE","IMP_SizeWE","IMP_UpArrow","InkMousePointer","InkMousePointer enumeration [Tablet PC]","msinkaut/IMP_Arrow","msinkaut/IMP_ArrowHourglass","msinkaut/IMP_ArrowQuestion","msinkaut/IMP_Crosshair","msinkaut/IMP_Custom","msinkaut/IMP_Default","msinkaut/IMP_Hand","msinkaut/IMP_Hourglass","msinkaut/IMP_Ibeam","msinkaut/IMP_NoDrop","msinkaut/IMP_SizeAll","msinkaut/IMP_SizeNESW","msinkaut/IMP_SizeNS","msinkaut/IMP_SizeNWSE","msinkaut/IMP_SizeWE","msinkaut/IMP_UpArrow","msinkaut/InkMousePointer","tablet.inkmousepointer"]
old-location: tablet\inkmousepointer.htm
tech.root: tablet
ms.assetid: 74f489f2-d568-4133-96e6-de15cbfabfe7
ms.date: 12/05/2018
ms.keywords: 74f489f2-d568-4133-96e6-de15cbfabfe7, IMP_Arrow, IMP_ArrowHourglass, IMP_ArrowQuestion, IMP_Crosshair, IMP_Custom, IMP_Default, IMP_Hand, IMP_Hourglass, IMP_Ibeam, IMP_NoDrop, IMP_SizeAll, IMP_SizeNESW, IMP_SizeNS, IMP_SizeNWSE, IMP_SizeWE, IMP_UpArrow, InkMousePointer, InkMousePointer enumeration [Tablet PC], msinkaut/IMP_Arrow, msinkaut/IMP_ArrowHourglass, msinkaut/IMP_ArrowQuestion, msinkaut/IMP_Crosshair, msinkaut/IMP_Custom, msinkaut/IMP_Default, msinkaut/IMP_Hand, msinkaut/IMP_Hourglass, msinkaut/IMP_Ibeam, msinkaut/IMP_NoDrop, msinkaut/IMP_SizeAll, msinkaut/IMP_SizeNESW, msinkaut/IMP_SizeNS, msinkaut/IMP_SizeNWSE, msinkaut/IMP_SizeWE, msinkaut/IMP_UpArrow, msinkaut/InkMousePointer, tablet.inkmousepointer
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
req.typenames: InkMousePointer
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InkMousePointer
 - msinkaut/InkMousePointer
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
 - InkMousePointer
---

# InkMousePointer enumeration


## -description

Specifies the type of mouse pointer to appear.

## -enum-fields

### -field IMP_Default:0

 The default mouse pointer.

### -field IMP_Arrow:1

The arrow mouse pointer.

### -field IMP_Crosshair:2

The cross (cross-hair) mouse pointer.

### -field IMP_Ibeam:3

The I-beam mouse pointer.

### -field IMP_SizeNESW:4

The sizing handle NE/SW mouse pointer (double arrow that points northeast and southwest).

### -field IMP_SizeNS:5

The sizing handle N/S mouse pointer (double arrow that points north and south).

### -field IMP_SizeNWSE:6

The sizing handle NW/SE mouse pointer (double arrow that points northwest and southeast).

### -field IMP_SizeWE:7

The sizing handle W/E mouse pointer (double arrow that points west and east).

### -field IMP_UpArrow:8

The up arrow mouse pointer.

### -field IMP_Hourglass:9

The hourglass (wait) mouse pointer.

### -field IMP_NoDrop:10

The no-drop mouse pointer.

### -field IMP_ArrowHourglass:11

The arrow and hourglass mouse pointer.

### -field IMP_ArrowQuestion:12

The arrow and question mark mouse pointer.

### -field IMP_SizeAll:13

The size-all mouse pointer.

### -field IMP_Hand:14

The hand mouse pointer.

### -field IMP_Custom:99

The custom mouse pointer that the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mouseicon">MouseIcon</a> property specifies.

## -see-also

<a href="/windows/desktop/tablet/inkcollector-class">InkCollector Class</a>



<a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit Control Reference</a>



<a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture Control Reference</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer">MousePointer Property</a>
