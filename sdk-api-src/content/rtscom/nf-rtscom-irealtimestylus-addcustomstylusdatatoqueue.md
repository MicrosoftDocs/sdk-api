---
UID: NF:rtscom.IRealTimeStylus.AddCustomStylusDataToQueue
title: IRealTimeStylus::AddCustomStylusDataToQueue (rtscom.h)
author: windows-sdk-content
description: Adds custom data to the specified queue of the RealTimeStylus Class object.
old-location: tablet\irealtimestylus_addcustomstylusdatatoqueue.htm
tech.root: tablet
ms.assetid: 9d216853-9103-4027-a724-f35d84553a9b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 9d216853-9103-4027-a724-f35d84553a9b, AddCustomStylusDataToQueue, AddCustomStylusDataToQueue method [Tablet PC], AddCustomStylusDataToQueue method [Tablet PC],IRealTimeStylus interface, IRealTimeStylus interface [Tablet PC],AddCustomStylusDataToQueue method, IRealTimeStylus.AddCustomStylusDataToQueue, IRealTimeStylus::AddCustomStylusDataToQueue, rtscom/IRealTimeStylus::AddCustomStylusDataToQueue, tablet.irealtimestylus_addcustomstylusdatatoqueue
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
req.lib: 
req.dll: RTSCom.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RTSCom.dll
api_name:
 - IRealTimeStylus.AddCustomStylusDataToQueue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRealTimeStylus::AddCustomStylusDataToQueue


## -description



Adds custom data to the specified queue of the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object.




## -parameters




### -param sq [in]

The <a href="https://msdn.microsoft.com/245f1c78-a6e9-4138-bddb-c0c890583aea">StylusQueue Enumeration</a> specifying the stylus queue to which to add the custom data.


### -param pGuidId [in]

 The GUID for the data to add to the queue specified in <i>sq</i>.


### -param cbData [in]

 The size, in chars, of the data that <i>pbData</i> points to and which is to be added to the specified queue.


### -param pbData [in]

The custom data to add to the specified queue. May not be <b>NULL</b>.
          


## -returns



For a description of the return values, see <a href="https://msdn.microsoft.com/fc0900b4-f08b-4a93-bbc0-d3db067d7917">RealTimeStylus Classes and Interfaces</a>.




## -remarks



Specify which queue to add the data to with the <i>sq</i> parameter. Identify the data by using its GUID.

The <i>sq</i> parameter specifies where to add the custom data. It specifies adding the custom data as one of the following:

<ul>
<li>The next packet to be processed in the Input queue.</li>
<li>A packet to be added to the output queue before the packet currently being processed.</li>
<li>A packet to be added to the output queue after the packet currently being processed in the queue.</li>
</ul>
When data is added to the input queue, it is automatically added to the output queue. The order of the inserted data can only be controlled on the output queue by passing <b>AsyncStylusQueueImmediate</b> in the <i>sq</i> parameter.

The GUID can be used by objects other than plug-ins and real time styluses to add customized information to the queue. This method can be called from any object that has a reference to the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object. The calling object does not have to be a plug-in.

<b>IRealTimeStylus::AddCustomStylusDataToQueue Method</b> enables you to add functionality, such as selection and erase.




## -see-also




<a href="https://msdn.microsoft.com/938e1eb2-3dd4-4e21-9c46-9ef840172b05">DynamicRenderer Class</a>



<a href="https://msdn.microsoft.com/bfd13012-decf-423a-bc1a-39fb9b0eb64e">IRealTimeStylus</a>



<a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a>



<a href="https://msdn.microsoft.com/245f1c78-a6e9-4138-bddb-c0c890583aea">StylusQueue Enumeration</a>
 

 

