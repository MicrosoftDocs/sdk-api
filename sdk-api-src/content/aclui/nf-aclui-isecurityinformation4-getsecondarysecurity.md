---
UID: NF:aclui.ISecurityInformation4.GetSecondarySecurity
title: ISecurityInformation4::GetSecondarySecurity
author: windows-sdk-content
description: Returns additional security contexts that may impact access to the resource.
old-location: security\isecurityinformation4_getsecondarysecurity.htm
old-project: SecAuthZ
ms.assetid: 20BD7D3B-1097-45CF-8237-0FBAD6BD6E3E
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetSecondarySecurity, GetSecondarySecurity method [Security], GetSecondarySecurity method [Security],ISecurityInformation4 interface, ISecurityInformation4 interface [Security],GetSecondarySecurity method, ISecurityInformation4.GetSecondarySecurity, ISecurityInformation4::GetSecondarySecurity, aclui/ISecurityInformation4::GetSecondarySecurity, security.isecurityinformation4_getsecondarysecurity
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: aclui.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: SI_PAGE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Aclui.h
api_name:
 - ISecurityInformation4.GetSecondarySecurity
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ISecurityInformation4::GetSecondarySecurity


## -description


The <b>GetSecondarySecurity</b> method returns additional security contexts that may impact access to the resource.


## -parameters




### -param pSecurityObjects [out]

An array of <a href="https://msdn.microsoft.com/C3E61527-76AB-49E9-8BBD-486F437CC677">SECURITY_OBJECT</a> structures that contain the secondary security objects associated with the resources that are set on success. The array is owned by the caller and is freed by using the <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> function. The <b>pwszName</b> member is also freed by using <b>LocalFree</b>. If the <b>cbData</b> or <b>cbData2</b> members of the <b>SECURITY_OBJECT</b> structure are not zero, then the caller must free the corresponding <b>pData</b> or <b>pData2</b> by using <b>LocalFree</b>. If either of those members are zero, then the corresponding <b>pData</b> and <b>pData2</b> members are owned by the resource manager and must remain valid until the <a href="https://msdn.microsoft.com/756c94b0-946f-47eb-b4b4-db3e6e89fe46">EditSecurity</a> function returns


### -param pSecurityObjectCount [out]

The number of security objects in the <i>pSecurityObjects</i> parameter that are set on success.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



A resource manager does not need to return secondary objects with the <b>fWellKnown</b> member set to <b>TRUE</b> and the <b>Id</b> member set to SECURITY_OBJECT_ID_OBJECT_SD, SECURITY_OBJECT_ID_CENTRAL_POLICY, or SECURITY_OBJECT_ID_CENTRAL_ACCESS_RULE. Security objects with these IDs will be provided by the access control editor when calling <a href="https://msdn.microsoft.com/03B73103-D7C0-4BA2-B315-3CC0049B1B8E">ComputeEffectivePermissionWithSecondarySecurity</a>.

Interpretation of the returned security objects is tied to the implementation of <a href="https://msdn.microsoft.com/03B73103-D7C0-4BA2-B315-3CC0049B1B8E">ComputeEffectivePermissionWithSecondarySecurity</a>.




## -see-also




<a href="https://msdn.microsoft.com/F7AD3612-5D66-49DB-81EF-040849D32CB4">ISecurityInformation4</a>
 

 

