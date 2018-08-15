---
UID: NF:manipulations.IManipulationProcessor.ProcessMoveWithTime
title: IManipulationProcessor::ProcessMoveWithTime
author: windows-sdk-content
description: Feeds movement data, including a time stamp, for the target object to its manipulation processor.
old-location: wintouch\imanpiulationprocessor_processmovewithtime.htm
old-project: wintouch
ms.assetid: 0840ef85-9b18-4248-96fe-93653274a89a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IManipulationProcessor interface [Windows Touch],ProcessMoveWithTime method, IManipulationProcessor.ProcessMoveWithTime, IManipulationProcessor::ProcessMoveWithTime, ProcessMoveWithTime, ProcessMoveWithTime method [Windows Touch], ProcessMoveWithTime method [Windows Touch],IManipulationProcessor interface, manipulations/IManipulationProcessor::ProcessMoveWithTime, wintouch.imanpiulationprocessor_processmovewithtime
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: manipulations.h
req.include-header: Manipulations_i.c
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MANIPULATION_PROCESSOR_MANIPULATIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - manipulations.h
api_name:
 - IManipulationProcessor.ProcessMoveWithTime
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IManipulationProcessor::ProcessMoveWithTime


## -description


Feeds movement data, including a time stamp, for the target object to its manipulation processor.


## -parameters




### -param manipulatorId

The identifier for the touch contact to be processed.


### -param x

The horizontal coordinate data associated with the target.


### -param y

The vertical coordinate data associated with the target.


### -param timestamp

The time of the data event.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an HRESULT error code such as <b>E_FAIL</b>.




## -remarks



It is possible to receive touch events out of the order they were produced.  To fix this, 
    you should extract the time stamp from the <a href="https://msdn.microsoft.com/fc382759-3a1e-401e-a6a7-1bf209a5434b">TOUCHINPUT</a> structure when you process events.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
static void ProcessMove(TOUCHINPUT* pTouchInput, IManipulationProcessor* pManipulationProcessor){
  pManipulationProcessor-&gt;ProcessMoveWithTime(
    pTouchInput-&gt;dwID, 
    static_cast&lt;float&gt;(pTouchInput-&gt;x), 
    static_cast&lt;float&gt;(pTouchInput-&gt;y), 
    pTouchInput-&gt;dwTime
  );
}
      </pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/963f87c1-e128-4bd5-9f28-d49418f768fb">IManipulationProcessor</a>



<a href="https://msdn.microsoft.com/33736f79-cb61-449c-80b9-1358db2621e9">Methods</a>



<a href="https://msdn.microsoft.com/a76c9150-49b8-4a74-8ef0-bfa5ce9ec28a">ProcessDownWithTime</a>



<a href="https://msdn.microsoft.com/e2c0e975-3edd-43d5-8a58-2d8166413c76">ProcessMove</a>



<a href="https://msdn.microsoft.com/fafea353-9126-454d-9311-4859e5ae5712">ProcessUpWithTime</a>
 

 

