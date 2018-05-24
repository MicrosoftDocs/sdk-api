---
UID: NF:rtscom.IRealTimeStylus.GetStylusForId
title: IRealTimeStylus::GetStylusForId
author: windows-driver-content
description: Retrieves a stylus for the specified stylus identifier.
old-location: tablet\irealtimestylus_getstylusforid.htm
old-project: tablet
ms.assetid: 16218bd3-9e92-407b-99b1-155d4387641e
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: 16218bd3-9e92-407b-99b1-155d4387641e, GetStylusForId, GetStylusForId method [Tablet PC], GetStylusForId method [Tablet PC],IRealTimeStylus interface, IRealTimeStylus interface [Tablet PC],GetStylusForId method, IRealTimeStylus.GetStylusForId, IRealTimeStylus::GetStylusForId, rtscom/IRealTimeStylus::GetStylusForId, tablet.irealtimestylus_getstylusforid
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: rtscom.h
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
req.typenames: StylusQueue
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	RTSCom.dll
api_name:
-	IRealTimeStylus.GetStylusForId
product: Windows
targetos: Windows
req.lib: 
req.dll: RTSCom.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IRealTimeStylus::GetStylusForId


## -description



Retrieves a stylus for the specified stylus identifier.




## -parameters




### -param sid [in]

Specifies security identifier (SID) for the collection.


### -param ppiInkCursor [out, retval]

When this method returns, contains a pointer to an IInkCursor that describes the stylus for the <i>sid</i> parameter.


## -returns



For a description of the return values, see <a href="https://msdn.microsoft.com/fc0900b4-f08b-4a93-bbc0-d3db067d7917">RealTimeStylus Classes and Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/bfd13012-decf-423a-bc1a-39fb9b0eb64e">IRealTimeStylus</a>



<a href="https://msdn.microsoft.com/1e838591-ce9e-4f3f-9b5e-b8414faac6ba">IRealTimeStylus::GetStyluses Method</a>



<a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a>
 

 

