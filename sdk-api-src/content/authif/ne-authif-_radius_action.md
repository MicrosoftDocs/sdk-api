---
UID: NE:authif._RADIUS_ACTION
title: "_RADIUS_ACTION"
author: windows-sdk-content
description: The RADIUS_ACTION type enumerates the responses that a NPS Extension DLL can generate in response to an Access-Request.
old-location: nps\IAS_radius_action.htm
old-project: Nps
ms.assetid: c0bd58ca-24e5-4cee-95e9-521d15c44814
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: "*PRADIUS_ACTION, PRADIUS_ACTION, PRADIUS_ACTION enumeration pointer [Network Policy Server], RADIUS_ACTION, RADIUS_ACTION enumeration [Network Policy Server], _RADIUS_ACTION, _ias_radius_action, authif/PRADIUS_ACTION, authif/RADIUS_ACTION, authif/raAccept, authif/raContinue, authif/raReject, ias.radius_action, nps.IAS_radius_action, raAccept, raContinue, raReject"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
req.typenames: RADIUS_ACTION, *PRADIUS_ACTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	AuthIf.h
api_name:
-	RADIUS_ACTION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _RADIUS_ACTION enumeration


## -description


<div class="alert"><b>Note</b>  Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.  The content of this topic applies to both IAS and NPS. Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</div><div> </div>The 
<b>RADIUS_ACTION</b> type enumerates the responses that a NPS Extension DLL can generate in response to an Access-Request.


## -enum-fields




### -field raContinue

NPS continues to process the request. NPS also continues to call 
<a href="https://msdn.microsoft.com/75af0d43-f866-4769-8221-45e47c588bb0">RadiusExtensionProcess</a> in other Extension DLLs.


### -field raReject

Return an Access-Reject packet. The Access-Request is declined. In this case, NPS does not call 
<a href="https://msdn.microsoft.com/75af0d43-f866-4769-8221-45e47c588bb0">RadiusExtensionProcess</a> in any other Extension DLLs.


### -field raAccept

NPS accepts the Access-Request. NPS does not continue to call 
<a href="https://msdn.microsoft.com/75af0d43-f866-4769-8221-45e47c588bb0">RadiusExtensionProcess</a> in this case. However, it does continue to obtain authorizations for the user requesting access.


## -remarks



Use the values for this enumeration only as the actions for the 
<a href="https://msdn.microsoft.com/75af0d43-f866-4769-8221-45e47c588bb0">RadiusExtensionProcess</a> and 
<a href="https://msdn.microsoft.com/7525b719-5741-4256-8759-421a407b9e44">RadiusExtensionProcessEx</a> functions.




## -see-also




<a href="https://msdn.microsoft.com/3d4d8d22-4cd3-48e0-b4a4-dfa0a0b7b87f">About NPS Extensions</a>



<a href="https://msdn.microsoft.com/6bf9c421-f0f6-4c75-bb4d-dbe91dcb8d01">NPS Extensions Enumerations</a>



<a href="https://msdn.microsoft.com/2b7a16cb-bc64-4e81-8149-82f51c451312">NPS Extensions Reference</a>



<a href="https://msdn.microsoft.com/75af0d43-f866-4769-8221-45e47c588bb0">RadiusExtensionProcess</a>



<a href="https://msdn.microsoft.com/7525b719-5741-4256-8759-421a407b9e44">RadiusExtensionProcessEx</a>
 

 

