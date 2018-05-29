---
UID: NS:ocidl.tagQACONTROL
title: tagQACONTROL
author: windows-sdk-content
description: Specifies control information for IQuickActivate::QuickActivate.
old-location: com\qacontrol.htm
old-project: com
ms.assetid: dd7ee4b1-2ad9-4ceb-b569-9988696760e8
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: QACONTROL, QACONTROL structure [COM], _ctrl_QACONTROL, com.qacontrol, ocidl/QACONTROL, tagQACONTROL
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: QACONTROL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	OCIdl.h
api_name:
-	QACONTROL
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# tagQACONTROL structure


## -description


Specifies control information for  <a href="https://msdn.microsoft.com/504cb272-da1c-4ffb-b4b1-fdf288901660">IQuickActivate::QuickActivate</a>.


## -struct-fields




### -field cbSize

The size of the structure, in bytes.


### -field dwMiscStatus

The control's miscellaneous status bits that can also be returned by <a href="https://msdn.microsoft.com/0c5e9f73-8eec-48e0-a172-4d3d49e56071">IOleObject::GetMiscStatus</a>. See <a href="https://msdn.microsoft.com/0a90d126-fc28-460c-8eaf-cf98ae998f95">OLEMISC</a> for more information.


### -field dwViewStatus

The control's view status that can also be returned by <a href="https://msdn.microsoft.com/cf8ec90c-07bb-4f60-93c9-4cee3fb5a056">IViewObjectEx::GetViewStatus</a>. See <a href="https://msdn.microsoft.com/7b3118af-db29-4eb1-9b1b-38a8ebe42f19">VIEWSTATUS</a> for more information.


### -field dwEventCookie

A unique identifier for control-defined events.


### -field dwPropNotifyCookie

A unique identifier for control-defined properties.


### -field dwPointerActivationPolicy

The control's activation policy that can also be returned by <a href="https://msdn.microsoft.com/bbdea7e1-620f-4b2b-8ac9-77061b8cfc1a">IPointerInactive::GetActivationPolicy</a>. If all the bits of <b>dwPointerActivationPolicy</b> are set, then the IPointerInactive interface may not be supported. The container should <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> to obtain the interface pointer in the standard manner.


## -see-also




<a href="https://msdn.microsoft.com/504cb272-da1c-4ffb-b4b1-fdf288901660">IQuickActivate::QuickActivate</a>
 

 

