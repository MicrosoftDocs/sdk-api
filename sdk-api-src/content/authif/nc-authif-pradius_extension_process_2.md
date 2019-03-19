---
UID: NC:authif.PRADIUS_EXTENSION_PROCESS_2
title: PRADIUS_EXTENSION_PROCESS_2 (authif.h)
author: windows-sdk-content
description: An application defined-function and is called by NPS for each authentication or accounting packet that NPS receives.
old-location: nps\IAS_radiusextensionprocess2.htm
tech.root: Nps
ms.assetid: 993b1ded-9fa9-4834-a37d-4da9e8ed9640
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PRADIUS_EXTENSION_PROCESS_2, PRADIUS_EXTENSION_PROCESS_2 callback, PRADIUS_EXTENSION_PROCESS_2 callback function [Network Policy Server], RadiusExtensionProcess2, authif/PRADIUS_EXTENSION_PROCESS_2, nps.IAS_radiusextensionprocess2
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
 - AuthIf.h
api_name:
 - PRADIUS_EXTENSION_PROCESS_2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PRADIUS_EXTENSION_PROCESS_2 callback function


## -description


<div class="alert"><b>Note</b>  Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.  The content of this topic applies to both IAS and NPS. Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</div><div> </div>The 
<i>RadiusExtensionProcess2</i> function is an application defined-function and is called by NPS for each authentication or accounting packet that NPS receives from the network access server (NAS). This function is similar to 
<a href="https://msdn.microsoft.com/75af0d43-f866-4769-8221-45e47c588bb0">RadiusExtensionProcess</a>. However, 
<i>RadiusExtensionProcess2</i> enables an Extension DLL to add, modify, and remove attributes to and from the authentication request or response.


## -parameters




### -param pECB [in, out]

Pointer to a 
<a href="https://msdn.microsoft.com/13ff0645-d3f8-4220-a5bc-11bb515bca95">RADIUS_EXTENSION_CONTROL_BLOCK</a> structure. The members of this structure contain values and function pointers that enable the NPS Extension DLL to process the RADIUS packet.


## -returns



If the function succeeds, the return value is <b>NO_ERROR</b>.

If the function fails, the return value should be an appropriate error code from WinError.h.




## -remarks



If the return value is anything other than <b>NO_ERROR</b>, NPS discards the request.

The following attributes are read-only. Extension DLLs that implement <i>RadiusExtensionProcess2</i> cannot add, modify, or remove  these attributes within a request or response contained in a <a href="https://msdn.microsoft.com/13ff0645-d3f8-4220-a5bc-11bb515bca95">RADIUS_EXTENSION_CONTROL_BLOCK</a>.

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
<a href="https://msdn.microsoft.com/fbbd9031-3ebe-47b8-8d8b-e359fa7d4b67">Setting Up the Extension  DLLs</a>.

NPS Extension DLLs that export 
<i>RadiusExtensionProcess2</i> do not need to export 
<a href="https://msdn.microsoft.com/2b76c648-a8d6-440c-b0b8-7c17f91ad961">RadiusExtensionFreeAttributes</a>.

For more information on the use of this function, see <a href="https://msdn.microsoft.com/6d738ad7-cce5-4835-97d6-c57173c79a16">NPS Extensions Process</a>.




## -see-also




<a href="https://msdn.microsoft.com/3d4d8d22-4cd3-48e0-b4a4-dfa0a0b7b87f">About NPS Extensions</a>



<a href="https://msdn.microsoft.com/ca217314-00f9-4f9d-a9fe-ed928b3c3b3d">NPS Extensions Functions</a>



<a href="https://msdn.microsoft.com/2b7a16cb-bc64-4e81-8149-82f51c451312">NPS Extensions Reference</a>



<a href="https://msdn.microsoft.com/75af0d43-f866-4769-8221-45e47c588bb0">RadiusExtensionProcess</a>



<a href="https://msdn.microsoft.com/7525b719-5741-4256-8759-421a407b9e44">RadiusExtensionProcessEx</a>
 

 

