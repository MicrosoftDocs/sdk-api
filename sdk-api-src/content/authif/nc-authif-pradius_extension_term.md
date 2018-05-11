---
UID: NC:authif.PRADIUS_EXTENSION_TERM
title: PRADIUS_EXTENSION_TERM
author: windows-driver-content
description: The RadiusExtensionTerm function is an application-defined function and is called by NPS prior to unloading the Extension DLL. Use RadiusExtensionTerm to perform any clean-up operations for the Extension DLL.
old-location: nps\IAS_radiusextensionterm.htm
old-project: Nps
ms.assetid: a3f6669f-bad5-4289-abbc-633851c1f5f8
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: PRADIUS_EXTENSION_TERM, PRADIUS_EXTENSION_TERM callback, RadiusExtensionTerm, RadiusExtensionTerm callback function [Network Policy Server], _ias_radiusextensionterm, authif/RadiusExtensionTerm, ias.radiusextensionterm, nps.IAS_radiusextensionterm
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: AUDIO_STREAM_CATEGORY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	AuthIf.h
api_name:
-	RadiusExtensionTerm
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PRADIUS_EXTENSION_TERM callback function


## -description


<div class="alert"><b>Note</b>  Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.  The content of this topic applies to both IAS and NPS. Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</div><div> </div>The 
<b>RadiusExtensionTerm</b> function is an application-defined function and is called by NPS prior to unloading the Extension DLL. Use 
<b>RadiusExtensionTerm</b> to perform any clean-up operations for the Extension DLL.


## -parameters




### -param Arg1








## -returns



This callback function does not return a value.




## -remarks



<b>RadiusExtensionTerm</b> is an optional function. The RADIUS Extension DLL need not implement 
<b>RadiusExtensionTerm</b>.




## -see-also




<a href="https://msdn.microsoft.com/3d4d8d22-4cd3-48e0-b4a4-dfa0a0b7b87f">About NPS Extensions</a>



<a href="https://msdn.microsoft.com/ca217314-00f9-4f9d-a9fe-ed928b3c3b3d">NPS Extensions Functions</a>



<a href="https://msdn.microsoft.com/2b7a16cb-bc64-4e81-8149-82f51c451312">NPS Extensions Reference</a>



<a href="https://msdn.microsoft.com/a463927f-550d-4078-8c0f-35c8742d887a">RadiusExtensionInit</a>
 

 

