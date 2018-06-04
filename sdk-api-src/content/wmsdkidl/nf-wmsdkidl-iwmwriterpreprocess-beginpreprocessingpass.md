---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IWMWriterPreprocess::BeginPreprocessingPass


## -description



The <b>BeginPreprocessingPass</b> method prepares the writer to begin preprocessing samples for the specified input stream.




## -parameters




### -param dwInputNum [in]

<b>DWORD</b> containing the input number that you want to preprocess.


### -param dwFlags [in]

Reserved. Set to zero.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>dwInputNum</i> specifies an invalid input number.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
The writer is not running.

OR

The preprocessor is neither waiting to be run nor stopped in the middle of a pass.

OR

The preprocessor has already made as many passes as specified by <a href="https://msdn.microsoft.com/81ff36e1-cce5-4c99-bf3a-ee2f1050c026">SetNumPreprocessingPasses</a>.

OR

The input specified is not supported for preprocessing.

</td>
</tr>
</table>
 




## -remarks



To successfully call <b>BeginPreprocessingPass</b>, the preprocessor must be set to make at least one preprocessing pass with a call to <b>SetNumPreprocessingPasses</b>.

The writer must be activated by calling <a href="https://msdn.microsoft.com/df511ff0-a87b-442a-85bd-c8d924ab2047">IWMWriter::BeginWriting</a> before you can call this method.




## -see-also




<a href="https://msdn.microsoft.com/06803639-3f21-4003-a460-16a0b5cc6d6f">IWMWriterPreprocess Interface</a>
 

 

