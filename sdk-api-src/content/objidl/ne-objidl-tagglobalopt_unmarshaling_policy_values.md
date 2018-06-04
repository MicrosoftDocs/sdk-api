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

# tagGLOBALOPT_UNMARSHALING_POLICY_VALUES enumeration


## -description


Provides values for the COM unmarshaling policy global option.


## -enum-fields




### -field COMGLB_UNMARSHALING_POLICY_NORMAL

Unmarshaling behavior is the same as versions before than Windows 8. <b>EOAC_NO_CUSTOM_MARSHAL</b> restrictions apply if this flag is set in <a href="https://msdn.microsoft.com/e0933741-6b75-4ce1-aa63-6240e4a7130f">CoInitializeSecurity</a>. Otherwise, there are no restrictions. This is the default for processes that aren't in the app container.


### -field COMGLB_UNMARSHALING_POLICY_STRONG

Unmarshaling allows only a system-trusted list of hardened unmarshalers and unmarshalers allowed per-process by the <a href="https://msdn.microsoft.com/4655C6B6-02CE-42B2-A157-0C0325D1BE52">CoAllowUnmarshalerCLSID</a> function. This is the default for processes in the app container.


### -field COMGLB_UNMARSHALING_POLICY_HYBRID

Unmarshaling data whose source is app container allows only a system-trusted list of hardened unmarshalers and unmarshalers allowed per-process by the <a href="https://msdn.microsoft.com/4655C6B6-02CE-42B2-A157-0C0325D1BE52">CoAllowUnmarshalerCLSID</a> function. Unmarshaling behavior for data with a source that's not app container is unchanged from previous versions.


## -see-also




<a href="https://msdn.microsoft.com/c5e823be-521d-4eb4-8836-fdd2cac6f15d">IGlobalOptions</a>



<a href="https://msdn.microsoft.com/7C4A3982-3623-4F1F-929C-6D0503700450">IMarshalingStream</a>
 

 

