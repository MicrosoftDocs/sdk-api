---
UID: NS:commctrl.tagNMREBARSPLITTER
title: tagNMREBARSPLITTER
author: windows-sdk-content
description: Contains information used to handle an RBN_SPLITTERDRAG notification code.
old-location: controls\NMREBARSPLITTER.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\rebar\structures\nmrebarsplitter.htm
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: "*LPNMREBARSPLITTER, LPNMREBARSPLITTER, LPNMREBARSPLITTER structure pointer [Windows Controls], NMREBARSPLITTER, NMREBARSPLITTER structure [Windows Controls], _shell_NMREBARSPLITTER, _shell_NMREBARSPLITTER_cpp, commctrl/LPNMREBARSPLITTER, commctrl/NMREBARSPLITTER, controls.NMREBARSPLITTER, controls._shell_NMREBARSPLITTER, tagNMREBARSPLITTER"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: commctrl.h
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
req.typenames: NMREBARSPLITTER, *LPNMREBARSPLITTER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	NMREBARSPLITTER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# tagNMREBARSPLITTER structure


## -description


Contains information used to handle an <a href="https://msdn.microsoft.com/7827c971-6a92-452f-b961-1abe6ae66d2a">RBN_SPLITTERDRAG</a> notification code.


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>

An <a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a> structure that contains additional information about this notification. 


### -field rcSizing

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a></b>

An <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that indicates the size the rebar will be after the drag operation completes.

