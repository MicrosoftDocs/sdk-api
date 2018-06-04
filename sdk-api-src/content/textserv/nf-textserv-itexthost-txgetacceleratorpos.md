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

# ITextHost::TxGetAcceleratorPos


## -description


Requests the special character to use for the underlining accelerator character.


## -parameters




### -param pcp

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a>*</b>

The character position of the character to underline. This variable is set by the text host. A character position of 
					–1 (that is, negative one) indicates that no character should be underlined. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

The return value is <b>S_OK</b>. 




## -remarks



Accelerators allow keyboard shortcuts, or accelerator keys, to various UI elements (such as buttons). Typically, the shortcut character is underlined.

This method tells the text services object which character is the accelerator and thus should be underlined. Note that the text services object does 
				<i>not</i> process accelerators; that is the responsibility of the host.

This method is typically only called if the TXTBIT_SHOWACCELERATOR bit is set in the text services object. See <a href="https://msdn.microsoft.com/41ae1a84-e721-4666-bac0-eb11c9b55279">OnTxPropertyBitsChange</a>.

<div class="alert"><b>Note</b>  <i>Any</i> change to the text in the text services object results in the invalidation of the accelerator underlining. In this case, it is the host's responsibility to recalculate the appropriate character position and inform the text services object that a new accelerator is available.</div>
<div> </div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/28d86b94-2d36-4749-8954-3857bf6dbdac">ITextHost</a>



<a href="https://msdn.microsoft.com/41ae1a84-e721-4666-bac0-eb11c9b55279">OnTxPropertyBitsChange</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/71ecd220-ab1a-4caa-b1b9-0951e943692e">Windowless Rich Edit Controls</a>
 

 

