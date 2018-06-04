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

# IWbemClassObject::GetObjectText


## -description


The 
<b>IWbemClassObject::GetObjectText</b> method returns a textual rendering of the object in the MOF syntax. Notice that the MOF text returned does not contain all the information about the object, but only enough information for the MOF compiler to be able to re-create the original object. For instance, no propagated qualifiers or parent class properties are displayed.


## -parameters




### -param lFlags [in]

Normally 0. If <b>WBEM_FLAG_NO_FLAVORS</b> is specified, qualifiers will be presented without propagation or flavor information.


### -param pstrObjectText [out]

This must point to <b>NULL</b> on entry. This parameter receives from Windows Management a newly allocated <b>BSTR</b> that was initialized with <b>SysAllocString</b>. You must call <b>SysFreeString</b> on the pointer when the string is no longer required. This pointer points to a MOF syntax rendering of the object upon return from the call. Because this is an out parameter, the pointer must not point to a string that is valid before this method is called, because the pointer will not be deallocated.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>. For general <b>HRESULT</b> values, see <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



The following algorithm is used to reconstruct the text of the parameters of a method:

<ol>
<li>Parameters are resequenced in the order of their identifier values.</li>
<li>Parameters that are specified as [in] and [out] will be combined into a single parameter.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a>



<a href="https://msdn.microsoft.com/8b36bd32-4931-4641-a019-cbaa3547edd0">IWbemQualifierSet</a>



<a href="https://msdn.microsoft.com/6E4F87D1-9952-4D85-9A32-3D7068831087">WBEM_TEXT_FLAG_TYPE</a>
 

 

