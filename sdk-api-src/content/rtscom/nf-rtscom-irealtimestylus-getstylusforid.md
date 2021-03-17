---
UID: NF:rtscom.IRealTimeStylus.GetStylusForId
title: IRealTimeStylus::GetStylusForId (rtscom.h)
description: Retrieves a stylus for the specified stylus identifier.
helpviewer_keywords: ["16218bd3-9e92-407b-99b1-155d4387641e","GetStylusForId","GetStylusForId method [Tablet PC]","GetStylusForId method [Tablet PC]","IRealTimeStylus interface","IRealTimeStylus interface [Tablet PC]","GetStylusForId method","IRealTimeStylus.GetStylusForId","IRealTimeStylus::GetStylusForId","rtscom/IRealTimeStylus::GetStylusForId","tablet.irealtimestylus_getstylusforid"]
old-location: tablet\irealtimestylus_getstylusforid.htm
tech.root: tablet
ms.assetid: 16218bd3-9e92-407b-99b1-155d4387641e
ms.date: 12/05/2018
ms.keywords: 16218bd3-9e92-407b-99b1-155d4387641e, GetStylusForId, GetStylusForId method [Tablet PC], GetStylusForId method [Tablet PC],IRealTimeStylus interface, IRealTimeStylus interface [Tablet PC],GetStylusForId method, IRealTimeStylus.GetStylusForId, IRealTimeStylus::GetStylusForId, rtscom/IRealTimeStylus::GetStylusForId, tablet.irealtimestylus_getstylusforid
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
req.lib: 
req.dll: RTSCom.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRealTimeStylus::GetStylusForId
 - rtscom/IRealTimeStylus::GetStylusForId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RTSCom.dll
api_name:
 - IRealTimeStylus.GetStylusForId
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

For a description of the return values, see <a href="/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>.

## -see-also

<a href="/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus">IRealTimeStylus</a>



<a href="/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-getstyluses">IRealTimeStylus::GetStyluses Method</a>



<a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a>