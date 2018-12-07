---
UID: NF:manipulations.IInertiaProcessor.Reset
title: IInertiaProcessor::Reset
author: windows-sdk-content
description: The Reset method initializes the processor with initial timestamp and restarts inertia.
old-location: wintouch\iinertiaprocessor_reset.htm
tech.root: wintouch
ms.assetid: 69ce260d-0674-4ff0-8610-bc814976bd3d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IInertiaProcessor interface [Windows Touch],Reset method, IInertiaProcessor.Reset, IInertiaProcessor::Reset, Reset, Reset method [Windows Touch], Reset method [Windows Touch],IInertiaProcessor interface, manipulations/IInertiaProcessor::Reset, wintouch.iinertiaprocessor_reset
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: manipulations.h
req.include-header: Manipulations.h
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
 - IInertiaProcessor.Reset
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInertiaProcessor::Reset


## -description


The <b>Reset</b> method initializes the processor with initial timestamp and restarts inertia.


## -parameters






## -returns



Returns <b>S_OK</b> on success, otherwise returns an error code such as <b>E_FAIL</b>.




## -remarks



If you have changed properties on an object currently being manipulated by inertia, call <a href="https://msdn.microsoft.com/ff41789c-afc5-419b-9767-e99572b9b41e">Complete</a> before calling <b>Reset</b>.
	 


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
    // set properties on the IInertiaProcessor interface
    this-&gt;m_spIInertProc-&gt;put_DesiredRotation(spin);    
	 
    // complete any unprocessed inertia
    this-&gt;m_spIInertProc-&gt;Complete();
	 
    // reset the processor
    this-&gt;m_spIInertProc-&gt;Reset();		  
	 
    // If you have implemented a timer that handles inertia processing,
    // this should be started as well and the processor will raise
    // Manipulation* events
		  </pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ff41789c-afc5-419b-9767-e99572b9b41e">Complete</a>



<a href="https://msdn.microsoft.com/8dc171eb-0c6e-41dd-b506-5f91ea703a53">IInertiaProcessor</a>



<a href="https://msdn.microsoft.com/e4acfcac-06c1-42a5-9722-4534a4492ab8">Methods</a>
 

 

