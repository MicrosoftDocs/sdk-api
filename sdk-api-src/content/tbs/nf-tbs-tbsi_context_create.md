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

# Tbsi_Context_Create function


## -description


Creates a context handle that can be used to pass commands to TBS.


## -parameters




### -param pContextParams [in]

A parameter to a <a href="https://msdn.microsoft.com/1b2093b3-6e5e-4289-9b1b-48027ded0fac">TBS_CONTEXT_PARAMS</a> structure that contains the parameters associated with the context. 


### -param phContext [out]

A pointer to a location to store the new context handle.


## -returns



If the function succeeds, the function returns TBS_SUCCESS.

If the function fails, it returns a TBS return code that indicates the error.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TBS_SUCCESS</b></dt>
<dt>0 (0x0)</dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TBS_E_BAD_PARAMETER</b></dt>
<dt>2150121474 (0x80284002)</dt>
</dl>
</td>
<td width="60%">
One or more parameter values are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TBS_E_INTERNAL_ERROR</b></dt>
<dt>2150121473 (0x80284001)</dt>
</dl>
</td>
<td width="60%">
An internal software error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TBS_E_INVALID_CONTEXT_PARAM</b></dt>
<dt>2150121479 (0x80284007)</dt>
</dl>
</td>
<td width="60%">
A context parameter that is not valid was passed when attempting to create a TBS context.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TBS_E_INVALID_OUTPUT_POINTER</b></dt>
<dt>2150121475 (0x80284003)</dt>
</dl>
</td>
<td width="60%">
A specified output pointer is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TBS_E_SERVICE_DISABLED</b></dt>
<dt>2150121488 (0x80284010)</dt>
</dl>
</td>
<td width="60%">
The TBS service has been disabled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TBS_E_SERVICE_NOT_RUNNING</b></dt>
<dt>2150121480 (0x80284008)</dt>
</dl>
</td>
<td width="60%">
The TBS service is not running and could not be started.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TBS_E_SERVICE_START_PENDING</b></dt>
<dt>2150121483 (0x8028400B)</dt>
</dl>
</td>
<td width="60%">
The TBS service has been started but is not yet running.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TBS_E_TOO_MANY_TBS_CONTEXTS</b></dt>
<dt>2150121481 (0x80284009)</dt>
</dl>
</td>
<td width="60%">
A new context could not be created because there are too many open contexts.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TBS_E_TPM_NOT_FOUND</b></dt>
<dt>2150121487 (0x8028400F)</dt>
</dl>
</td>
<td width="60%">
A compatible Trusted Platform Module (TPM) Security Device cannot be found on this computer.

</td>
</tr>
</table>
 




## -remarks



The <i>pContextParams</i> parameter allows the caller to specify which TPM version (TPM1.2 or TPM2.0) it is designed for. For applications interacting with version 1.2 TPM only, a pointer to a <a href="https://msdn.microsoft.com/1b2093b3-6e5e-4289-9b1b-48027ded0fac">TBS_CONTEXT_PARAMS</a> structure can be provided, with the version field set to TPM_VERSION_12.
Applications interacting with version 2.0 TPM will pass a pointer to a <a href="https://msdn.microsoft.com/B113B422-A66E-4498-99DA-65D4ED0B84B1">TBS_CONTEXT_PARAMS2</a> structure, with the version field set to TPM_VERSION_20. Set the reserved field to 0, and the <b>includeTPm20</b> field to 1. If the application is prepared to interact with a version 1.2 TPM as well (in case the system has no version 2.0 TPM), set the <b>includeTpm12</b> field to 1.


If no TPM is present on the system, or the TPM version does not match those requested by the caller, <b>Tbsi_Context_Create</b> will return the TBS_E_TPM_NOT_FOUND (0x8028400) error code.  Application programs must check for both versions and be able to interact with either TPM.



