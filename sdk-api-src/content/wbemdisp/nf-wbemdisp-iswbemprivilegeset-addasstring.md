---
UID: NF:wbemdisp.ISWbemPrivilegeSet.AddAsString
title: ISWbemPrivilegeSet::AddAsString
author: windows-sdk-content
description: You can use the AddAsString method of the SWbemPrivilegeSet object to add a privilege to an SWbemPrivilegeSet collection using a privilege string.
old-location: wmi\swbemprivilegeset_addasstring.htm
old-project: WmiSdk
ms.assetid: 729ed4e3-2c5c-4bb4-acc6-cf9ad0d5eaf1
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: AddAsString, AddAsString method [Windows Management Instrumentation], AddAsString method [Windows Management Instrumentation],ISWbemPrivilegeSet interface, AddAsString method [Windows Management Instrumentation],SWbemPrivilegeSet object, ISWbemPrivilegeSet interface [Windows Management Instrumentation],AddAsString method, ISWbemPrivilegeSet.AddAsString, ISWbemPrivilegeSet::AddAsString, SWbemPrivilegeSet object [Windows Management Instrumentation],AddAsString method, SWbemPrivilegeSet.AddAsString, _hmm_swbemprivilegeset.addasstring, wmi.swbemprivilegeset_addasstring
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wbemdisp.h
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
req.type-library: Wbemdisp.tlb
tech.root: 
req.typenames: WbemTimeout
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemdisp.dll
api_name:
 - SWbemPrivilegeSet.AddAsString
 - ISWbemPrivilegeSet.AddAsString
 - ISWbemPrivilegeSet.AddAsString
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemPrivilegeSet::AddAsString


## -description


You can use the 
<b>AddAsString</b> method of the 
<a href="https://msdn.microsoft.com/073cf2d4-f7ee-45a6-8fa6-ca77a4870346">SWbemPrivilegeSet</a> object to add a privilege to an <b>SWbemPrivilegeSet</b> collection using a privilege string. Use this method to add a privilege or to enable a privilege for <a href="https://msdn.microsoft.com/794587fa-5feb-455b-be28-ecfaa25625ad">SWbemSecurity</a> objects. See <a href="https://msdn.microsoft.com/65b923d5-5244-498d-9644-d4978fb84f85">Executing Privileged Operations Using VBScript</a>.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param strPrivilege

Required. One of the privilege strings. For a complete list of these strings and the associated WMI constants, see 
<a href="https://msdn.microsoft.com/f9400597-81bb-44a8-80dc-aba0160aea26">Privilege Constants</a>. Every privilege string represents a specific privilege. For example, to add the privilege that use to shut down a computer system, use the <b>SeShutdownPrivilege</b> string.


### -param bIsEnabled [optional]

Boolean value that enables or disables this privilege. The default value is <b>True</b>.


### -param objWbemPrivilege






## -returns



If successful, this method returns an <a href="https://msdn.microsoft.com/18ee4587-6347-4075-b5e9-c5fb02f3cbf7">SWbemPrivilege</a> object that represents the new privilege. Otherwise, a null object is returned.




## -see-also




<a href="https://msdn.microsoft.com/11bb8723-f329-4083-8219-2256ce44a5e3">Executing Privileged Operations</a>



<a href="https://msdn.microsoft.com/65b923d5-5244-498d-9644-d4978fb84f85">Executing Privileged Operations Using VBScript</a>



<a href="https://msdn.microsoft.com/f9400597-81bb-44a8-80dc-aba0160aea26">Privilege Constants</a>



<a href="https://msdn.microsoft.com/073cf2d4-f7ee-45a6-8fa6-ca77a4870346">SWbemPrivilegeSet</a>



<a href="https://msdn.microsoft.com/7d44193f-60e1-4e83-8640-31d8df509d98">SWbemPrivilegeSet.Add</a>



<a href="https://msdn.microsoft.com/4c0b6d49-262c-4840-955b-35b16b68f29f">SWbemPrivilegeSet.Remove</a>



<a href="https://msdn.microsoft.com/235a1115-d8c4-4334-a4e0-fc539da4d2ae">WbemPrivilegeEnum</a>
 

 

