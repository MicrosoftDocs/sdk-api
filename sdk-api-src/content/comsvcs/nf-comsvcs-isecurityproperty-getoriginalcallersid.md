---
UID: NF:comsvcs.ISecurityProperty.GetOriginalCallerSID
title: ISecurityProperty::GetOriginalCallerSID
author: windows-sdk-content
description: Retrieves the security identifier of the base process that initiated the call sequence from which the current method was called.
old-location: cos\isecurityproperty_getoriginalcallersid.htm
old-project: cossdk
ms.assetid: e8700635-94cb-4d1a-9325-f93d00c5181f
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: GetOriginalCallerSID, GetOriginalCallerSID method [COM+], GetOriginalCallerSID method [COM+],ISecurityProperty interface, ISecurityProperty interface [COM+],GetOriginalCallerSID method, ISecurityProperty.GetOriginalCallerSID, ISecurityProperty::GetOriginalCallerSID, _cos_ISecurityProperty_GetOriginalCallerSID, comsvcs/ISecurityProperty::GetOriginalCallerSID, cos.isecurityproperty_getoriginalcallersid
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ISecurityProperty.GetOriginalCallerSID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ISecurityProperty::GetOriginalCallerSID


## -description


Retrieves the security identifier of the base process that initiated the call sequence from which the 
    current method was called.

The preferred way to obtain information about the original caller is to use the 
    <a href="https://msdn.microsoft.com/cd96ef31-784f-40fa-beb5-92a88823326b">ISecurityCallContext</a> interface.


## -parameters




### -param pSID [out]

A reference to the security ID of the base process that initiated the call sequence from which the current 
      method was called.


## -returns



This method can return the standard return values <b>E_INVALIDARG</b>, 
      <b>E_OUTOFMEMORY</b>, <b>E_UNEXPECTED</b>, and 
      <b>E_FAIL</b>, as well as the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The security ID of the base process that originated the call into the current object is returned in the 
        parameter <i>pSid</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CONTEXT_E_NOCONTEXT</b></dt>
</dl>
</td>
<td width="60%">
The current object does not have a context associated with it because either the component was not 
        imported into an application or the object was not created with one of the COM+ 
        <b>CreateInstance</b> methods.

</td>
</tr>
</table>
 




## -remarks



You use the 
     <b>GetOriginalCallerSID</b> method to 
     determine the security ID of the original process that initiated the call sequence from which the current method 
     was called, not the originator (or creator) of the process. Although a pointer to an object can be passed through 
     a series of servers and users, 
     <b>GetOriginalCallerSID</b> always 
     returns the first server and user of the process, even if that user was not the original creator of the object. 
     The following scenario illustrates the functionality of the 
     <b>GetOriginalCallerSID</b> method.

<img alt="" src="./images/ff4d2c22-6e80-48e0-a6ca-4622b703e9e9.png"/>

<ol>
<li>Base Process 1, running on Server A as user A, creates Object X, on Server B, running as user B.</li>
<li>Base Process 1 passes its reference on Object X to Base Process 2, running on Server D as user D.</li>
<li>Base Process 2 uses that reference to call into Object X.</li>
<li>Object X calls into Object Y, running on Server C. If Object Y then calls 
      <b>GetOriginalCallerSID</b>, the 
      security ID of user D is returned, not user A, who originally created the object.</li>
</ol>
<div class="alert"><b>Note</b>  Usually, an object's original caller is the same process as its original creator. The only situation in 
     which the original caller and the original creator would be different is one in which the original creator passes 
     a reference to another process and the other process initiates the call sequence (as in the preceding 
     example).</div>
<div> </div>
The path to the original caller is broken if any object along the chain was created by some means other than 
     <a href="https://msdn.microsoft.com/2e870191-5a34-490e-9f3a-cb646fe3f470">IObjectContext::CreateInstance</a> or 
     <a href="https://msdn.microsoft.com/3dc08700-0872-4d60-a968-cffed974c7b2">ITransactionContext::CreateInstance</a>. 
     For example, if Base Process 1 uses <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a> 
     to create Object X, when Object Y calls 
     <b>GetOriginalCallerSID</b> the security 
     ID it gets back is the security ID of user B, not user D. This is because the call sequence is traced back 
     through the objects' context and COM+ can create a context only for an object that is created with either 
     <b>IObjectContext::CreateInstance</b> or 
     <b>ITransactionContext::CreateInstance</b>.

You must call <a href="https://msdn.microsoft.com/572bf3fd-eb85-40de-b607-26b77b9d9cf8">ReleaseSID</a> on a security 
    ID when you finish using it.




## -see-also




<a href="https://msdn.microsoft.com/116715a5-a3e1-48aa-b155-107ea330b7ee">ISecurityProperty</a>
 

 

