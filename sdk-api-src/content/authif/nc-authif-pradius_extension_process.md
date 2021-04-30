---
UID: NC:authif.PRADIUS_EXTENSION_PROCESS
title: PRADIUS_EXTENSION_PROCESS (authif.h)
description: The RadiusExtensionProcess function is an application-defined function and is called by NPS for each authentication or accounting packet that NPS receives from the network access server (NAS).
helpviewer_keywords: ["PRADIUS_EXTENSION_PROCESS","PRADIUS_EXTENSION_PROCESS callback","PRADIUS_EXTENSION_PROCESS callback function [Network Policy Server]","RadiusExtensionProcess","_ias_radiusextensionprocess","authif/PRADIUS_EXTENSION_PROCESS","ias.radiusextensionprocess","nps.IAS_radiusextensionprocess"]
old-location: nps\IAS_radiusextensionprocess.htm
tech.root: Nps
ms.assetid: 75af0d43-f866-4769-8221-45e47c588bb0
ms.date: 12/05/2018
ms.keywords: PRADIUS_EXTENSION_PROCESS, PRADIUS_EXTENSION_PROCESS callback, PRADIUS_EXTENSION_PROCESS callback function [Network Policy Server], RadiusExtensionProcess, _ias_radiusextensionprocess, authif/PRADIUS_EXTENSION_PROCESS, ias.radiusextensionprocess, nps.IAS_radiusextensionprocess
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PRADIUS_EXTENSION_PROCESS
 - authif/PRADIUS_EXTENSION_PROCESS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - AuthIf.h
api_name:
 - PRADIUS_EXTENSION_PROCESS
---

# PRADIUS_EXTENSION_PROCESS callback function


## -description

<div class="alert"><b>Note</b>  Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.  The content of this topic applies to both IAS and NPS. Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</div><div> </div>The 
<b>RadiusExtensionProcess</b> function is an application-defined function and is called by NPS for each authentication or accounting packet that NPS receives from the network access server (NAS).

## -parameters

### -param pAttrs [in]

Pointer to an array of 
<a href="/windows/desktop/api/authif/ns-authif-radius_attribute">attributes</a> from the request. The array is terminated by an attribute with <b>dwAttrType</b> set to <b>ratMinimum</b>. These attributes should be treated as read-only; they should not be modified by 
<b>RadiusExtensionProcess</b>. Also, these attributes should not be referenced in any way after 
<b>RadiusExtensionProcess</b> returns.

### -param pfAction [out]

Pointer to a value of type 
<a href="/windows/desktop/api/authif/ne-authif-radius_action">RADIUS_ACTION</a>, initially set to <b>raContinue</b>. This parameter specifies the action that NPS should take in response to an Access-Request.

## -returns

If the function succeeds, the return value is <b>NO_ERROR</b>.

If the function fails, the return value should be an appropriate error code from Winerror.h.

## -remarks

If the return value is anything other than <b>NO_ERROR</b>, NPS discards the request.

NPS supports multiple Extension DLLs. NPS calls 
<b>RadiusExtensionProcess</b> for each of the DLLs listed in the registry. For more information see 
<a href="/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls">Setting Up the Extension DLLs</a>.

The Extension DLL may export 
<a href="/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex">RadiusExtensionProcessEx</a> instead of 
<b>RadiusExtensionProcess</b>. The Extension DLL may export 
<a href="/windows/desktop/api/authif/nc-authif-pradius_extension_process_2">RadiusExtensionProcess2</a>.

For more information on the use of this function, see <a href="/windows/desktop/Nps/ias-authentication-and-authorization-process">NPS Extensions Process</a>.

## -see-also

<a href="/windows/desktop/Nps/ias-about-internet-authentication-service">About NPS Extensions</a>



<a href="/windows/desktop/Nps/ias-internet-authentication-service-functions">NPS Extensions Functions</a>



<a href="/windows/desktop/Nps/ias-internet-authentication-service-reference">NPS Extensions Reference</a>



<a href="/windows/desktop/api/authif/ne-authif-radius_action">RADIUS_ACTION</a>



<a href="/windows/desktop/api/authif/ns-authif-radius_attribute">RADIUS_ATTRIBUTE</a>



<a href="/windows/desktop/api/authif/ne-authif-radius_attribute_type">RADIUS_ATTRIBUTE_TYPE</a>



<a href="/windows/desktop/api/authif/nc-authif-pradius_extension_process_2">RadiusExtensionProcess2</a>



<a href="/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex">RadiusExtensionProcessEx</a>
