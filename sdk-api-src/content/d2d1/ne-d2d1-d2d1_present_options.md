---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# D2D1_PRESENT_OPTIONS enumeration


## -description


Describes how a render target behaves when it presents its content. This enumeration allows a bitwise combination of its member values.


## -enum-fields




### -field D2D1_PRESENT_OPTIONS_NONE

The render target waits until the display refreshes to present and discards the frame upon presenting.


### -field D2D1_PRESENT_OPTIONS_RETAIN_CONTENTS

The render target does not discard the frame upon presenting.


### -field D2D1_PRESENT_OPTIONS_IMMEDIATELY

The render target does not wait until the display refreshes to present.


### -field D2D1_PRESENT_OPTIONS_FORCE_DWORD



