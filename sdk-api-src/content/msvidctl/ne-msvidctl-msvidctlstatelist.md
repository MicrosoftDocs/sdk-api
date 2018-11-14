---
UID: NE:msvidctl.MSVidCtlStateList
title: MSVidCtlStateList
author: windows-sdk-content
description: This topic applies to Windows XP or later.
old-location: mstv\msvidctlstatelist.htm
tech.root: MSTV
ms.assetid: b4da9c6e-3235-4c78-b9e1-57c9d06fccbc
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: MSVidCtlStateList, MSVidCtlStateList enumeration [Microsoft TV Technologies], MSVidCtlStateListEnumeration, STATE_PAUSE, STATE_PLAY, STATE_STOP, STATE_UNBUILT, enumeration [Microsoft TV Technologies], mstv.msvidctlstatelist, msvidctl/MSVidCtlStateList, msvidctl/STATE_PAUSE, msvidctl/STATE_PLAY, msvidctl/STATE_STOP, msvidctl/STATE_UNBUILT
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: msvidctl.h
req.include-header: Dshow.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - msvidctl.h
api_name:
 - MSVidCtlStateList
product: Windows
targetos: Windows
req.typenames: MSVidCtlStateList
req.redist: 
---

# MSVidCtlStateList enumeration


## -description



This topic applies to Windows XP or later.
        



The <b>MSVidCtlStateList</b> enumeration defines the possible state values of the Video Control or the underlying filter graph.


## -enum-fields




### -field STATE_UNBUILT

Indicates that there is no filter graph.


### -field STATE_STOP

Indicates that the Video Control is stopped.


### -field STATE_PAUSE

Indicates that the Video Control is paused.


### -field STATE_PLAY

Indicates that the Video Control is playing.


## -see-also




<a href="https://msdn.microsoft.com/0f7a5e37-5a0d-415e-aca0-df5f9448b017">IMSVidDeviceEvent::StateChange</a>



<a href="https://msdn.microsoft.com/3c21f2c6-8eff-4fe5-a383-057f3394d9ee">Video Control Enumerations</a>



<a href="https://msdn.microsoft.com/16dca4ab-be3d-493a-892b-8d90a0baf109">_IMSVidCtlEvents::StateChange</a>
 

 

