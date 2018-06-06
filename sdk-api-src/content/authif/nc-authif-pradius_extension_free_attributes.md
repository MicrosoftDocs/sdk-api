---
UID: NC:authif.PRADIUS_EXTENSION_FREE_ATTRIBUTES
title: PRADIUS_EXTENSION_FREE_ATTRIBUTES
author: windows-sdk-content
description: The RadiusExtensionFreeAttributes function is an application-defined function and is called by NPS to free the memory occupied by attributes returned by RadiusExtensionProcessEx.
old-location: nps\IAS_radiusextensionfreeattributes.htm
old-project: Nps
ms.assetid: 2b76c648-a8d6-440c-b0b8-7c17f91ad961
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: PRADIUS_EXTENSION_FREE_ATTRIBUTES, PRADIUS_EXTENSION_FREE_ATTRIBUTES callback, PRADIUS_EXTENSION_FREE_ATTRIBUTES callback function [Network Policy Server], RadiusExtensionFreeAttributes, _ias_radiusextensionfreeattributes, authif/PRADIUS_EXTENSION_FREE_ATTRIBUTES, ias.radiusextensionfreeattributes, nps.IAS_radiusextensionfreeattributes
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AUDIO_STREAM_CATEGORY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - AuthIf.h
api_name:
 - PRADIUS_EXTENSION_FREE_ATTRIBUTES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PRADIUS_EXTENSION_FREE_ATTRIBUTES callback function


## -description


<div class="alert"><b>Note</b>  Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.  The content of this topic applies to both IAS and NPS. Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</div><div> </div>The 
<b>RadiusExtensionFreeAttributes</b> function is an application-defined function and is called by NPS to free the memory occupied by attributes returned by 
<a href="https://msdn.microsoft.com/7525b719-5741-4256-8759-421a407b9e44">RadiusExtensionProcessEx</a>.


## -parameters




### -param pAttrs

Pointer to an array of attributes. The 
<b>RadiusExtensionFreeAttributes</b> function should deallocate the memory occupied by these attributes.

These attributes were returned in the <i>pOutAttrs</i> parameter in a previous call to the 
<a href="https://msdn.microsoft.com/7525b719-5741-4256-8759-421a407b9e44">RadiusExtensionProcessEx</a> function.


## -returns



This callback function does not return a value.




## -remarks



If you implement 
<a href="https://msdn.microsoft.com/7525b719-5741-4256-8759-421a407b9e44">RadiusExtensionProcessEx</a>, you must also implement 
<b>RadiusExtensionFreeAttributes</b>.




## -see-also




<a href="https://msdn.microsoft.com/3d4d8d22-4cd3-48e0-b4a4-dfa0a0b7b87f">About NPS Extensions</a>



<a href="https://msdn.microsoft.com/ca217314-00f9-4f9d-a9fe-ed928b3c3b3d">NPS Extensions Functions</a>



<a href="https://msdn.microsoft.com/2b7a16cb-bc64-4e81-8149-82f51c451312">NPS Extensions Reference</a>



<a href="https://msdn.microsoft.com/7525b719-5741-4256-8759-421a407b9e44">RadiusExtensionProcessEx</a>
 

 

