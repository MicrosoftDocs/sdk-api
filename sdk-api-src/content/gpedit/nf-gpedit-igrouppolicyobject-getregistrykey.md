---
UID: NF:gpedit.IGroupPolicyObject.GetRegistryKey
title: IGroupPolicyObject::GetRegistryKey method
author: windows-driver-content
description: The GetRegistryKey method retrieves a handle to the root of the registry key for the specified GPO section.
old-location: policy\igrouppolicyobject_getregistrykey.htm
old-project: Policy
ms.assetid: 6d46aeb4-8675-4746-9b80-46a0def184b8
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GPO_SECTION_MACHINE, GPO_SECTION_ROOT, GetRegistryKey method [Group Policy], GetRegistryKey method [Group Policy], IGroupPolicyObject interface, GetRegistryKey,IGroupPolicyObject.GetRegistryKey, IGroupPolicyObject, IGroupPolicyObject interface [Group Policy], GetRegistryKey method, IGroupPolicyObject::GetRegistryKey, _win32_igrouppolicyobject_getregistrykey, gpedit/IGroupPolicyObject::GetRegistryKey, policy.igrouppolicyobject_getregistrykey
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gpedit.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gpedit.dll
api_name:
-	IGroupPolicyObject.GetRegistryKey
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpedit.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGroupPolicyObject::GetRegistryKey method


## -description


The
    <b>GetRegistryKey</b> method retrieves a handle to the root of the registry key for the specified GPO section.


## -parameters




### -param dwSection [in]

Specifies the GPO section. This parameter can be one of the following values.



#### GPO_SECTION_ROOT

Root section



#### GPO_SECTION_MACHINE

Computer section


### -param hKey [out]

Receives a handle to the registry key. This handle is opened with all access rights. For more information, see 
<a href="https://msdn.microsoft.com/266d5c8e-1bcd-48e5-bc06-2fbc956d8658">Registry Key Security and Access Rights</a>.


## -returns



If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the method returns one of the COM error codes defined in the Platform SDK header file WinError.h. If the registry information is not loaded, the method returns <b>E_FAIL</b>.




## -remarks



The registry handle is a handle to the root of the registry key. To get or set values in the 
Policies key, first call the 
<a href="https://msdn.microsoft.com/bad0a0f8-1889-4eff-98be-084c95d69f3b">RegOpenKey</a> function to open the <b>Software</b>\
Policies key.

When you have finished using the registry handle, call the 
<a href="https://msdn.microsoft.com/10175499-abf3-4694-9594-bb97b43f3fa5">RegCloseKey</a> function to close the handle.




## -see-also




<a href="https://msdn.microsoft.com/dc15a69d-a44d-4731-a9e5-6165abd581c4">Group Policy
    Interfaces</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy
    Overview</a>



<a href="https://msdn.microsoft.com/b3cd31a1-c238-4eb2-8164-9c4891e6227b">IGroupPolicyObject</a>
 

 

