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

# IWbemContext::SetValue


## -description


The 
<b>IWbemContext::SetValue</b> method creates or overwrites a named context value.


## -parameters




### -param wszName




### -param lFlags [in]

Reserved. This parameter must be 0 (zero).


### -param pValue [in]

Must point to a valid <b>VARIANT</b>, which is treated as read-only. The value in the <b>VARIANT</b> becomes the named context value. An entire 
<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a> object can be stored as well as a simple value by enclosing it in a <b>VARIANT</b> that uses the <b>VT_UNKNOWN</b> type. The caller must execute <a href="_com_iunknown_queryinterface">QueryInterface</a> on the 
<b>IWbemClassObject</b> object by asking for <b>IID_IUnknown</b>, and by using the returned pointer in the <b>VARIANT</b>.

If <i>pValue</i> is to contain an embedded 
<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a> object, the caller must call <a href="_com_iunknown_queryinterface">IWbemClassObject::QueryInterface</a> for <b>IID_IUnknown</b> and place the resulting pointer in the <b>VARIANT</b> by using a type of <b>VT_UNKNOWN</b>. The original embedded object is copied during the write operation, and so cannot be modified by the operation.


#### - strName [in]

Cannot be <b>NULL</b>. It is a read-only pointer that  indicates the context value name. This value must be <b>null</b>-terminated.


## -returns



This method returns an <b>HRESULT</b> that indicates the status of a method call. The following list lists and describes the values contained in an <b>HRESULT</b>.




## -see-also




<a href="https://msdn.microsoft.com/458bd455-6984-414b-a0b7-62887d9dad7c">IWbemContext</a>



<a href="https://msdn.microsoft.com/e11fff37-aeb7-41c5-8639-ca0a7a144263">IWbemContext::GetValue</a>
 

 

