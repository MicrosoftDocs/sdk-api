---
UID: NC:authif.PRADIUS_EXTENSION_PROCESS_EX
title: PRADIUS_EXTENSION_PROCESS_EX (authif.h)
author: windows-sdk-content
description: The RadiusExtensionProcessEx function is an application-defined function and is called by NPS for each authentication or accounting packet that NPS receives from the network access server (NAS).
old-location: nps\IAS_radiusextensionprocessex.htm
tech.root: Nps
ms.assetid: 7525b719-5741-4256-8759-421a407b9e44
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PRADIUS_EXTENSION_PROCESS_EX, PRADIUS_EXTENSION_PROCESS_EX callback, PRADIUS_EXTENSION_PROCESS_EX callback function [Network Policy Server], RadiusExtensionProcessEx, _ias_radiusextensionprocessex, authif/PRADIUS_EXTENSION_PROCESS_EX, ias.radiusextensionprocessex, nps.IAS_radiusextensionprocessex
ms.topic: callback
req.header: authif.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
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
 - UserDefined
api_location:
 - Authif.h
api_name:
 - PRADIUS_EXTENSION_PROCESS_EX
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PRADIUS_EXTENSION_PROCESS_EX callback function


## -description


<div class="alert"><b>Note</b>  Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.  The content of this topic applies to both IAS and NPS. Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</div><div> </div>The 
<i>RadiusExtensionProcessEx</i> function is an application-defined function and is called by NPS for each authentication or accounting packet that NPS receives from the network access server (NAS). This function is similar to 
<a href="https://msdn.microsoft.com/75af0d43-f866-4769-8221-45e47c588bb0">RadiusExtensionProcess</a>. However, 
<i>RadiusExtensionProcessEx</i> enables the Extension DLL to append attributes to the authentication response.


## -parameters




### -param *pInAttrs [in]

Pointer to an array of 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">attributes</a> from the request. The array is terminated by an attribute with <b>dwAttrType</b> set to <b>ratMinimum</b>. These attributes should be treated as read-only; they should not be modified by 
<i>RadiusExtensionProcessEx</i>. Also, these attributes should not be referenced in any way after 
<i>RadiusExtensionProcessEx</i> returns.


### -param *pOutAttrs [out]

Pointer to an array of 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">attributes</a> provided by the NPS Extension DLL. The array is terminated by an attribute with <b>dwAttrType</b> set to <b>ratMinimum</b>. NPS  adds these attributes to the authentication response.

The NPS Extension DLL allocates the memory for the array of attributes. NPS calls 
<a href="https://msdn.microsoft.com/2b76c648-a8d6-440c-b0b8-7c17f91ad961">RadiusExtensionFreeAttributes</a> to free the memory occupied by the array of attributes.


### -param pfAction [out]

Pointer to a value of type 
<a href="https://msdn.microsoft.com/c0bd58ca-24e5-4cee-95e9-521d15c44814">RADIUS_ACTION</a>, initially set to <b>raContinue</b>. This parameter specifies the action that NPS should take in response to an Access-Request.


## -returns



If the function succeeds, the return value is <b>NO_ERROR</b>.

If the function fails, the return value should be an appropriate error code from WinError.h.




## -remarks



If the return value is anything other than <b>NO_ERROR</b>, NPS discards the request.

NPS supports multiple Extension DLLs. NPS calls 
<i>RadiusExtensionProcessEx</i> for each of the DLLs listed in the registry. For more information see 
<a href="https://msdn.microsoft.com/fbbd9031-3ebe-47b8-8d8b-e359fa7d4b67">Setting Up the Extension DLLs</a>.

NPS calls 
<a href="https://msdn.microsoft.com/2b76c648-a8d6-440c-b0b8-7c17f91ad961">RadiusExtensionFreeAttributes</a> to free the memory occupied by the array of attributes returned by 
<i>RadiusExtensionProcessEx</i>. For this reason, if you implement 
<i>RadiusExtensionProcessEx</i>, you must also implement 
<b>RadiusExtensionFreeAttributes</b>.

For more information on the use of this function, see <a href="https://msdn.microsoft.com/6d738ad7-cce5-4835-97d6-c57173c79a16">NPS Extensions Process</a>.




## -see-also




<a href="https://msdn.microsoft.com/3d4d8d22-4cd3-48e0-b4a4-dfa0a0b7b87f">About NPS Extensions</a>



<a href="https://msdn.microsoft.com/ca217314-00f9-4f9d-a9fe-ed928b3c3b3d">NPS Extensions Functions</a>



<a href="https://msdn.microsoft.com/2b7a16cb-bc64-4e81-8149-82f51c451312">NPS Extensions Reference</a>



<a href="https://msdn.microsoft.com/c0bd58ca-24e5-4cee-95e9-521d15c44814">RADIUS_ACTION</a>



<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a>



<a href="https://msdn.microsoft.com/b0b39062-0622-48f8-a06a-232713ec8c3c">RADIUS_ATTRIBUTE_TYPE</a>



<a href="https://msdn.microsoft.com/75af0d43-f866-4769-8221-45e47c588bb0">RadiusExtensionProcess</a>
 

 

