---
UID: NF:aclui.ISecurityInformation3.GetFullResourceName
title: ISecurityInformation3::GetFullResourceName (aclui.h)
author: windows-sdk-content
description: Retrieves the full path and file name of the object associated with the access control editor that is displayed by calling the OpenElevatedEditor method.
old-location: security\isecurityinformation3_getfullresourcename.htm
tech.root: SecAuthZ
ms.assetid: a22b9a75-6aa8-4b32-8d86-7fb21afd248f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetFullResourceName, GetFullResourceName method [Security], GetFullResourceName method [Security],ISecurityInformation3 interface, ISecurityInformation3 interface [Security],GetFullResourceName method, ISecurityInformation3.GetFullResourceName, ISecurityInformation3::GetFullResourceName, aclui/ISecurityInformation3::GetFullResourceName, security.isecurityinformation3_getfullresourcename
ms.topic: method
req.header: aclui.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - COM
api_location:
 - Aclui.h
api_name:
 - ISecurityInformation3.GetFullResourceName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISecurityInformation3::GetFullResourceName


## -description


The <b>GetFullResourceName</b> method retrieves the full path and file name of the object associated with the access control editor that is displayed by calling the <a href="https://msdn.microsoft.com/4ed50e6b-4c4a-48bf-ad7c-133064a4be47">OpenElevatedEditor</a> method.


## -parameters




### -param ppszResourceName [out]

The full path and file name of the object for which permissions are to be edited.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/e6cf92da-ebd2-4960-9df1-7124745df616">ISecurityInformation3</a>



<a href="https://msdn.microsoft.com/4ed50e6b-4c4a-48bf-ad7c-133064a4be47">OpenElevatedEditor</a>
 

 

