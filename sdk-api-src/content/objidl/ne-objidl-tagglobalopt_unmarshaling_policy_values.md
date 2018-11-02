---
UID: NE:objidl.tagGLOBALOPT_UNMARSHALING_POLICY_VALUES
title: tagGLOBALOPT_UNMARSHALING_POLICY_VALUES
author: windows-sdk-content
description: Provides values for the COM unmarshaling policy global option.
old-location: com\globalopt_unmarshaling_policy_values.htm
tech.root: com
ms.assetid: 7F557290-7162-4B32-880B-9A445A083F91
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: COMGLB_UNMARSHALING_POLICY_HYBRID, COMGLB_UNMARSHALING_POLICY_NORMAL, COMGLB_UNMARSHALING_POLICY_STRONG, GLOBALOPT_UNMARSHALING_POLICY_VALUES, GLOBALOPT_UNMARSHALING_POLICY_VALUES enumeration [COM], com.globalopt_unmarshaling_policy_values, objidl/COMGLB_UNMARSHALING_POLICY_HYBRID, objidl/COMGLB_UNMARSHALING_POLICY_NORMAL, objidl/COMGLB_UNMARSHALING_POLICY_STRONG, objidl/GLOBALOPT_UNMARSHALING_POLICY_VALUES, tagGLOBALOPT_UNMARSHALING_POLICY_VALUES
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: objidl.h
req.include-header: Objidlbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidlbase.idl
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
 - HeaderDef
api_location:
 - objidl.h
api_name:
 - GLOBALOPT_UNMARSHALING_POLICY_VALUES
product: Windows
targetos: Windows
req.typenames: GLOBALOPT_UNMARSHALING_POLICY_VALUES
req.redist: 
---

# tagGLOBALOPT_UNMARSHALING_POLICY_VALUES enumeration


## -description


Provides values for the COM unmarshaling policy global option.


## -enum-fields




### -field COMGLB_UNMARSHALING_POLICY_NORMAL

Unmarshaling behavior is the same as versions older than Windows 8. <b>EOAC_NO_CUSTOM_MARSHAL</b> restrictions apply if this flag is set in <a href="https://msdn.microsoft.com/e0933741-6b75-4ce1-aa63-6240e4a7130f">CoInitializeSecurity</a>. Otherwise, there are no restrictions. This is the default for processes that aren't in the app container.


### -field COMGLB_UNMARSHALING_POLICY_STRONG

Unmarshaling allows only a system-trusted list of hardened unmarshalers and unmarshalers allowed per-process by the <a href="https://msdn.microsoft.com/4655C6B6-02CE-42B2-A157-0C0325D1BE52">CoAllowUnmarshalerCLSID</a> function. This is the default for processes in the app container.


### -field COMGLB_UNMARSHALING_POLICY_HYBRID

Unmarshaling data whose source is app container allows only a system-trusted list of hardened unmarshalers and unmarshalers allowed per-process by the <a href="https://msdn.microsoft.com/4655C6B6-02CE-42B2-A157-0C0325D1BE52">CoAllowUnmarshalerCLSID</a> function. Unmarshaling behavior for data with a source that's not app container is unchanged from previous versions.


## -see-also




<a href="https://msdn.microsoft.com/c5e823be-521d-4eb4-8836-fdd2cac6f15d">IGlobalOptions</a>



<a href="https://msdn.microsoft.com/7C4A3982-3623-4F1F-929C-6D0503700450">IMarshalingStream</a>
 

 

