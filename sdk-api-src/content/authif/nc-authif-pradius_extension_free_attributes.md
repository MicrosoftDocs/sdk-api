---
UID: NC:authif.PRADIUS_EXTENSION_FREE_ATTRIBUTES
title: PRADIUS_EXTENSION_FREE_ATTRIBUTES (authif.h)
author: windows-sdk-content
description: The RadiusExtensionFreeAttributes function is an application-defined function and is called by NPS to free the memory occupied by attributes returned by RadiusExtensionProcessEx.
old-location: nps\IAS_radiusextensionfreeattributes.htm
tech.root: Nps
ms.assetid: 2b76c648-a8d6-440c-b0b8-7c17f91ad961
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PRADIUS_EXTENSION_FREE_ATTRIBUTES, PRADIUS_EXTENSION_FREE_ATTRIBUTES callback, PRADIUS_EXTENSION_FREE_ATTRIBUTES callback function [Network Policy Server], RadiusExtensionFreeAttributes, _ias_radiusextensionfreeattributes, authif/PRADIUS_EXTENSION_FREE_ATTRIBUTES, ias.radiusextensionfreeattributes, nps.IAS_radiusextensionfreeattributes
ms.topic: callback
f1_keywords: 
 - "authif/PRADIUS_EXTENSION_FREE_ATTRIBUTES"
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
 - AuthIf.h
api_name:
 - PRADIUS_EXTENSION_FREE_ATTRIBUTES
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PRADIUS_EXTENSION_FREE_ATTRIBUTES callback function


## -description


<div class="alert"><b>Note</b>  Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.  The content of this topic applies to both IAS and NPS. Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</div><div> </div>The 
<b>RadiusExtensionFreeAttributes</b> function is an application-defined function and is called by NPS to free the memory occupied by attributes returned by 
<a href="https://docs.microsoft.com/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex">RadiusExtensionProcessEx</a>.


## -parameters




### -param pAttrs

Pointer to an array of attributes. The 
<b>RadiusExtensionFreeAttributes</b> function should deallocate the memory occupied by these attributes.

These attributes were returned in the <i>pOutAttrs</i> parameter in a previous call to the 
<a href="https://docs.microsoft.com/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex">RadiusExtensionProcessEx</a> function.


## -returns



This callback function does not return a value.




## -remarks



If you implement 
<a href="https://docs.microsoft.com/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex">RadiusExtensionProcessEx</a>, you must also implement 
<b>RadiusExtensionFreeAttributes</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Nps/ias-about-internet-authentication-service">About NPS Extensions</a>



<a href="https://docs.microsoft.com/windows/desktop/Nps/ias-internet-authentication-service-functions">NPS Extensions Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/Nps/ias-internet-authentication-service-reference">NPS Extensions Reference</a>



<a href="https://docs.microsoft.com/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex">RadiusExtensionProcessEx</a>
 

 

