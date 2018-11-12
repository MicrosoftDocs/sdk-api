---
UID: NF:wmcontainer.IMFASFStreamSelector.SetOutputMutexSelection
title: IMFASFStreamSelector::SetOutputMutexSelection
author: windows-sdk-content
description: Selects a mutual exclusion record to use for a mutual exclusion object associated with an output.
old-location: mf\imfasfstreamselector_setoutputmutexselection.htm
tech.root: medfound
ms.assetid: eebaf4a4-fcd5-4438-82ec-e9da2de6b0fd
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: IMFASFStreamSelector interface [Media Foundation],SetOutputMutexSelection method, IMFASFStreamSelector.SetOutputMutexSelection, IMFASFStreamSelector::SetOutputMutexSelection, SetOutputMutexSelection, SetOutputMutexSelection method [Media Foundation], SetOutputMutexSelection method [Media Foundation],IMFASFStreamSelector interface, eebaf4a4-fcd5-4438-82ec-e9da2de6b0fd, mf.imfasfstreamselector_setoutputmutexselection, wmcontainer/IMFASFStreamSelector::SetOutputMutexSelection
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmcontainer.h
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
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFASFStreamSelector.SetOutputMutexSelection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFASFStreamSelector::SetOutputMutexSelection


## -description



Selects a mutual exclusion record to use for a mutual exclusion object associated with an output.




## -parameters




### -param dwOutputNum [in]

The output number for which to set a stream.


### -param dwMutexNum [in]

Index of the mutual exclusion for which to select.


### -param wSelectedRecord [in]

Record of the specified mutual exclusion to select.


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
</table>
 




## -remarks



An output is a stream in an Advanced Systems Format (ASF) data section that will be parsed. If mutual exclusion is used, mutually exclusive streams share the same output.

An ASF file can contain multiple mutually exclusive relationships, such as a file with both language based and bit-rate based mutual exclusion. If an output is involved in multiple mutually exclusive relationships, a record from each must be selected.




## -see-also




<a href="https://msdn.microsoft.com/d2e1fc15-2e12-4698-a4b1-ca8046d228de">IMFASFStreamSelector</a>



<a href="https://msdn.microsoft.com/d134f4a9-9bca-454f-8dc1-2e152684a4bf">IMFASFStreamSelector::GetOutputMutex</a>
 

 

