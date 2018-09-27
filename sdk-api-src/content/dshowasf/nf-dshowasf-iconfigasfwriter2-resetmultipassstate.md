---
UID: NF:dshowasf.IConfigAsfWriter2.ResetMultiPassState
title: IConfigAsfWriter2::ResetMultiPassState
author: windows-sdk-content
description: The ResetMultiPassState method resets the filter when a preprocessing encoding pass is canceled before it is completed.
old-location: dshow\iconfigasfwriter2_resetmultipassstate.htm
tech.root: DirectShow
ms.assetid: ca2ec239-ffb9-4030-9160-77a0c9be0a07
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: IConfigAsfWriter2 interface [DirectShow],ResetMultiPassState method, IConfigAsfWriter2.ResetMultiPassState, IConfigAsfWriter2::ResetMultiPassState, IConfigAsfWriter2ResetMultiPassState, ResetMultiPassState, ResetMultiPassState method [DirectShow], ResetMultiPassState method [DirectShow],IConfigAsfWriter2 interface, dshow.iconfigasfwriter2_resetmultipassstate, dshowasf/IConfigAsfWriter2::ResetMultiPassState
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dshowasf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - Dshowasf.h
api_name:
 - IConfigAsfWriter2.ResetMultiPassState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IConfigAsfWriter2::ResetMultiPassState


## -description



The <code>ResetMultiPassState</code> method resets the filter when a preprocessing encoding pass is canceled before it is completed.




## -parameters






## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_STOPPED</b></dt>
</dl>
</td>
<td width="60%">
The filter was not in a stopped state.

</td>
</tr>
</table>
 




## -remarks



This method must be called to reset the internal state of the filter whenever a preprocessing encoding pass is canceled before the filter has received an <a href="https://msdn.microsoft.com/2029afc4-419c-494a-ae52-1f84b08bcb35">EC_PREPROCESS_COMPLETE</a> event. It is not necessary to call this method if the preprocessing encoding pass completes without errors.




## -see-also




<a href="https://msdn.microsoft.com/dffda43a-5831-4889-864f-81351b9e2bb3">Creating ASF Files in DirectShow</a>



<a href="https://msdn.microsoft.com/fd931a95-3678-46de-8f17-9e7c27087398">IConfigAsfWriter2 Interface</a>
 

 

