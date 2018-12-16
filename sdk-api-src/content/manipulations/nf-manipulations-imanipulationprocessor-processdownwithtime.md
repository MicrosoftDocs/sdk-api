---
UID: NF:manipulations.IManipulationProcessor.ProcessDownWithTime
title: IManipulationProcessor::ProcessDownWithTime
author: windows-sdk-content
description: Feeds touch down data, including a timestamp, to the manipulation processor associated with a target.
old-location: wintouch\imanpiulationprocessor_processdownwithtime.htm
tech.root: wintouch
ms.assetid: a76c9150-49b8-4a74-8ef0-bfa5ce9ec28a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IManipulationProcessor interface [Windows Touch],ProcessDownWithTime method, IManipulationProcessor.ProcessDownWithTime, IManipulationProcessor::ProcessDownWithTime, ProcessDownWithTime, ProcessDownWithTime method [Windows Touch], ProcessDownWithTime method [Windows Touch],IManipulationProcessor interface, manipulations/IManipulationProcessor::ProcessDownWithTime, wintouch.imanpiulationprocessor_processdownwithtime
ms.topic: method
req.header: manipulations.h
req.include-header: Manipulations_i.c
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - manipulations.h
api_name:
 - IManipulationProcessor.ProcessDownWithTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IManipulationProcessor::ProcessDownWithTime


## -description


Feeds touch down data, including a timestamp, to the manipulation processor associated with a target.


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
    you should extract the timestamp from the <a href="https://msdn.microsoft.com/fc382759-3a1e-401e-a6a7-1bf209a5434b">TOUCHINPUT</a> structure when you process events.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>static void ProcessDown(TOUCHINPUT* pTouchInput, IManipulationProcessor* pManipulationProcessor){
  pManipulationProcessor-&gt;ProcessDownWithTime(
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



<a href="https://msdn.microsoft.com/2c192bc4-6922-4c70-961d-1f8684ad792b">ProcessDown</a>



<a href="https://msdn.microsoft.com/0840ef85-9b18-4248-96fe-93653274a89a">ProcessMoveWithTime</a>



<a href="https://msdn.microsoft.com/fafea353-9126-454d-9311-4859e5ae5712">ProcessUpWithTime</a>
 

 

