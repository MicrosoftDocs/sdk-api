---
UID: NC:authif.PRADIUS_EXTENSION_PROCESS_2
title: PRADIUS_EXTENSION_PROCESS_2 (authif.h)
description: An application defined-function and is called by NPS for each authentication or accounting packet that NPS receives.
helpviewer_keywords: ["PRADIUS_EXTENSION_PROCESS_2","PRADIUS_EXTENSION_PROCESS_2 callback","PRADIUS_EXTENSION_PROCESS_2 callback function [Network Policy Server]","RadiusExtensionProcess2","authif/PRADIUS_EXTENSION_PROCESS_2","nps.IAS_radiusextensionprocess2"]
old-location: nps\IAS_radiusextensionprocess2.htm
tech.root: Nps
ms.assetid: 993b1ded-9fa9-4834-a37d-4da9e8ed9640
ms.date: 12/05/2018
ms.keywords: PRADIUS_EXTENSION_PROCESS_2, PRADIUS_EXTENSION_PROCESS_2 callback, PRADIUS_EXTENSION_PROCESS_2 callback function [Network Policy Server], RadiusExtensionProcess2, authif/PRADIUS_EXTENSION_PROCESS_2, nps.IAS_radiusextensionprocess2
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
 - PRADIUS_EXTENSION_PROCESS_2
 - authif/PRADIUS_EXTENSION_PROCESS_2
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
 - PRADIUS_EXTENSION_PROCESS_2
---

# PRADIUS_EXTENSION_PROCESS_2 callback function


## -description

<div class="alert"><b>Note</b>  Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.  The content of this topic applies to both IAS and NPS. Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</div><div> </div>The 
<i>RadiusExtensionProcess2</i> function is an application defined-function and is called by NPS for each authentication or accounting packet that NPS receives from the network access server (NAS). This function is similar to 
<a href="/windows/desktop/api/authif/nc-authif-pradius_extension_process">RadiusExtensionProcess</a>. However, 
<i>RadiusExtensionProcess2</i> enables an Extension DLL to add, modify, and remove attributes to and from the authentication request or response.

## -parameters

### -param pECB [in, out]

Pointer to a 
<a href="/windows/desktop/api/authif/ns-authif-radius_extension_control_block">RADIUS_EXTENSION_CONTROL_BLOCK</a> structure. The members of this structure contain values and function pointers that enable the NPS Extension DLL to process the RADIUS packet.

## -returns

If the function succeeds, the return value is <b>NO_ERROR</b>.

If the function fails, the return value should be an appropriate error code from WinError.h.

## -remarks

If the return value is anything other than <b>NO_ERROR</b>, NPS discards the request.

The following attributes are read-only. Extension DLLs that implement <i>RadiusExtensionProcess2</i> cannot add, modify, or remove  these attributes within a request or response contained in a <a href="/windows/desktop/api/authif/ns-authif-radius_extension_control_block">RADIUS_EXTENSION_CONTROL_BLOCK</a>.

<ul>
<li><b>ratCode</b></li>
<li><b>ratIdentifier</b></li>
<li><b>ratAuthenticator</b></li>
<li><b>ratSrcIPAddress</b></li>
<li><b>ratSrcPort</b></li>
<li><b>ratProvider</b></li>
<li><b>ratUniqueId</b></li>
<li><b>ratSrcIPv6Address</b></li>
</ul>
NPS supports multiple Extension DLLs. NPS calls 
<i>RadiusExtensionProcess2</i> for each of the DLLs listed in the registry. For more information see 
<a href="/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls">Setting Up the Extension  DLLs</a>.

NPS Extension DLLs that export 
<i>RadiusExtensionProcess2</i> do not need to export 
<a href="/windows/desktop/api/authif/nc-authif-pradius_extension_free_attributes">RadiusExtensionFreeAttributes</a>.

For more information on the use of this function, see <a href="/windows/desktop/Nps/ias-authentication-and-authorization-process">NPS Extensions Process</a>.

## -see-also

<a href="/windows/desktop/Nps/ias-about-internet-authentication-service">About NPS Extensions</a>



<a href="/windows/desktop/Nps/ias-internet-authentication-service-functions">NPS Extensions Functions</a>



<a href="/windows/desktop/Nps/ias-internet-authentication-service-reference">NPS Extensions Reference</a>



<a href="/windows/desktop/api/authif/nc-authif-pradius_extension_process">RadiusExtensionProcess</a>



<a href="/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex">RadiusExtensionProcessEx</a>