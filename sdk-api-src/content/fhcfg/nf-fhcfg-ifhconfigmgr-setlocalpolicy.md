---
UID: NF:fhcfg.IFhConfigMgr.SetLocalPolicy
title: IFhConfigMgr::SetLocalPolicy
author: windows-sdk-content
description: Changes the numeric parameter value of a local policy in an FhConfigMgr object.
old-location: winprog\ifhconfigmgr_setlocalpolicy.htm
old-project: DevNotes
ms.assetid: A1106349-6B14-4A44-B845-7853FA1919D6
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: FhConfigMgr class [Windows API],SetLocalPolicy method, IFhConfigMgr interface [Windows API],SetLocalPolicy method, IFhConfigMgr.SetLocalPolicy, IFhConfigMgr::SetLocalPolicy, SetLocalPolicy, SetLocalPolicy method [Windows API], SetLocalPolicy method [Windows API],FhConfigMgr class, SetLocalPolicy method [Windows API],IFhConfigMgr interface, fhcfg/IFhConfigMgr::SetLocalPolicy, winprog.ifhconfigmgr_setlocalpolicy
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: fhcfg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fhcfg.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: FH_TARGET_PROPERTY_TYPE, *PFH_TARGET_PROPERTY_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fhcfg.h
api_name:
 - IFhConfigMgr.SetLocalPolicy
 - FhConfigMgr.SetLocalPolicy
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# IFhConfigMgr::SetLocalPolicy


## -description


Changes the numeric parameter value of a local policy in an <a href="https://msdn.microsoft.com/CC97FC0F-3AA4-4D8A-81B3-14F68FDF5788">FhConfigMgr</a> object.


## -parameters




### -param LocalPolicyType [in]

Specifies the local policy.


### -param PolicyValue [in]

Specifies the new value of the numeric parameter for the specified local policy.


## -returns



<b>S_OK</b> on success, or an unsuccessful <b>HRESULT</b> value on failure. Possible unsuccessful <b>HRESULT</b> values include values defined in the FhErrors.h header file.




## -remarks



Each local policy contains a numeric parameter that specifies how or when the File History feature backs up files and folders. See the <a href="https://msdn.microsoft.com/59C54A67-91A3-495F-95F2-50EB373D442C">FH_LOCAL_POLICY_TYPE</a> enumeration for more information about the local policies that can be specified.

To retrieve the numeric parameter value for a local policy, use the <a href="https://msdn.microsoft.com/380B77C3-CA93-48D6-9915-FB788CF24C99">IFhConfigMgr::GetLocalPolicy</a> method.




## -see-also




<a href="https://msdn.microsoft.com/59C54A67-91A3-495F-95F2-50EB373D442C">FH_LOCAL_POLICY_TYPE</a>



<a href="https://msdn.microsoft.com/CC97FC0F-3AA4-4D8A-81B3-14F68FDF5788">FhConfigMgr</a>



<a href="https://msdn.microsoft.com/CDE8A011-6E78-49DF-A5E1-8E968355BA11">IFhConfigMgr</a>



<a href="https://msdn.microsoft.com/380B77C3-CA93-48D6-9915-FB788CF24C99">IFhConfigMgr::GetLocalPolicy</a>
 

 

