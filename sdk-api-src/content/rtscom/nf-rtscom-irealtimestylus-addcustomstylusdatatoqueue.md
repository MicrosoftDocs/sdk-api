---
UID: NF:rtscom.IRealTimeStylus.AddCustomStylusDataToQueue
title: IRealTimeStylus::AddCustomStylusDataToQueue (rtscom.h)
description: Adds custom data to the specified queue of the RealTimeStylus Class object.
helpviewer_keywords: ["9d216853-9103-4027-a724-f35d84553a9b","AddCustomStylusDataToQueue","AddCustomStylusDataToQueue method [Tablet PC]","AddCustomStylusDataToQueue method [Tablet PC]","IRealTimeStylus interface","IRealTimeStylus interface [Tablet PC]","AddCustomStylusDataToQueue method","IRealTimeStylus.AddCustomStylusDataToQueue","IRealTimeStylus::AddCustomStylusDataToQueue","rtscom/IRealTimeStylus::AddCustomStylusDataToQueue","tablet.irealtimestylus_addcustomstylusdatatoqueue"]
old-location: tablet\irealtimestylus_addcustomstylusdatatoqueue.htm
tech.root: tablet
ms.assetid: 9d216853-9103-4027-a724-f35d84553a9b
ms.date: 12/05/2018
ms.keywords: 9d216853-9103-4027-a724-f35d84553a9b, AddCustomStylusDataToQueue, AddCustomStylusDataToQueue method [Tablet PC], AddCustomStylusDataToQueue method [Tablet PC],IRealTimeStylus interface, IRealTimeStylus interface [Tablet PC],AddCustomStylusDataToQueue method, IRealTimeStylus.AddCustomStylusDataToQueue, IRealTimeStylus::AddCustomStylusDataToQueue, rtscom/IRealTimeStylus::AddCustomStylusDataToQueue, tablet.irealtimestylus_addcustomstylusdatatoqueue
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
 - IRealTimeStylus::AddCustomStylusDataToQueue
 - rtscom/IRealTimeStylus::AddCustomStylusDataToQueue
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
 - IRealTimeStylus.AddCustomStylusDataToQueue
---

# IRealTimeStylus::AddCustomStylusDataToQueue


## -description

Adds custom data to the specified queue of the <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object.

## -parameters

### -param sq [in]

The <a href="/windows/desktop/api/rtscom/ne-rtscom-stylusqueue">StylusQueue Enumeration</a> specifying the stylus queue to which to add the custom data.

### -param pGuidId [in]

 The GUID for the data to add to the queue specified in <i>sq</i>.

### -param cbData [in]

 The size, in chars, of the data that <i>pbData</i> points to and which is to be added to the specified queue.

### -param pbData [in]

The custom data to add to the specified queue. May not be <b>NULL</b>.

## -returns

For a description of the return values, see <a href="/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>.

## -remarks

Specify which queue to add the data to with the <i>sq</i> parameter. Identify the data by using its GUID.

The <i>sq</i> parameter specifies where to add the custom data. It specifies adding the custom data as one of the following:

<ul>
<li>The next packet to be processed in the Input queue.</li>
<li>A packet to be added to the output queue before the packet currently being processed.</li>
<li>A packet to be added to the output queue after the packet currently being processed in the queue.</li>
</ul>
When data is added to the input queue, it is automatically added to the output queue. The order of the inserted data can only be controlled on the output queue by passing <b>AsyncStylusQueueImmediate</b> in the <i>sq</i> parameter.

The GUID can be used by objects other than plug-ins and real time styluses to add customized information to the queue. This method can be called from any object that has a reference to the <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object. The calling object does not have to be a plug-in.

<b>IRealTimeStylus::AddCustomStylusDataToQueue Method</b> enables you to add functionality, such as selection and erase.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)">DynamicRenderer Class</a>



<a href="/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus">IRealTimeStylus</a>



<a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a>



<a href="/windows/desktop/api/rtscom/ne-rtscom-stylusqueue">StylusQueue Enumeration</a>