---
UID: NF:certenroll.IX509MachineEnrollmentFactory.CreateObject
title: IX509MachineEnrollmentFactory::CreateObject method
author: windows-driver-content
description: Creates an IX509EnrollmentHelper object on a webpage.
old-location: security\ix509machineenrollmentfactory_createobject.htm
old-project: SecCertEnroll
ms.assetid: f9a45219-1c88-4946-ad57-81b95c609066
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: CreateObject method [Security], CreateObject method [Security], IX509MachineEnrollmentFactory interface, CreateObject,IX509MachineEnrollmentFactory.CreateObject, IX509MachineEnrollmentFactory, IX509MachineEnrollmentFactory interface [Security], CreateObject method, IX509MachineEnrollmentFactory::CreateObject, certenroll/IX509MachineEnrollmentFactory::CreateObject, security.ix509machineenrollmentfactory_createobject
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Certenroll.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Certenroll.h
api_name:
-	IX509MachineEnrollmentFactory.CreateObject
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IX509MachineEnrollmentFactory::CreateObject method


## -description


The <b>CreateObject</b> method creates an <a href="https://msdn.microsoft.com/19124591-be1a-401e-9b83-c640d00de34a">IX509EnrollmentHelper</a> object on a webpage. This method is web enabled.


## -parameters




### -param strProgID [in]

A <b>BSTR</b> variable that contains the ProgID value. This must be "X509Enrollment.CX509EnrollmentHelper".


### -param ppIHelper [out, retval]

Address of a pointer to a variable that receives a pointer to an <a href="https://msdn.microsoft.com/19124591-be1a-401e-9b83-c640d00de34a">IX509EnrollmentHelper</a> interface.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table.  For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>strProgID</i> parameter cannot be <b>NULL</b> or empty.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The <i>strProgID</i> parameter must contain "X509Enrollment.CX509EnrollmentHelper".

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppIHelper</i> parameter cannot be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_ARITHMETIC_OVERFLOW)</b></dt>
</dl>
</td>
<td width="60%">
The <i>strProgID</i> parameter exceed 64,000 characters or contains embedded null characters.

</td>
</tr>
</table>
 




## -remarks



This method calls <a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a> on the <a href="https://msdn.microsoft.com/19124591-be1a-401e-9b83-c640d00de34a">IX509EnrollmentHelper</a> interface by using the <b>ContextAdministratorForceMachine</b> context value, thereby specifying that all certificates to be enrolled by the <a href="https://msdn.microsoft.com/8e262b4b-de6a-417e-9ade-0b451bd4c09a">IX509Enrollment2</a> object will be requested by an administrator acting on behalf of a computer. To enroll a user certificate, call <a href="https://msdn.microsoft.com/e865e499-1bfe-45c3-aeb3-3936f9173fd5">CreateObject</a> on the <a href="https://msdn.microsoft.com/f779c197-8467-481a-abf5-d3fd3ac90ba7">IX509EnrollmentWebClassFactory</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/2f97fdd7-13ca-4427-8ec5-24302d245fdb">IX509MachineEnrollmentFactory</a>
 

 

