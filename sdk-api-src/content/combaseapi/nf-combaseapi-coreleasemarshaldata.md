---
UID: NF:combaseapi.CoReleaseMarshalData
title: CoReleaseMarshalData function
author: windows-driver-content
description: Destroys a previously marshaled data packet.
old-location: com\coreleasemarshaldata.htm
old-project: com
ms.assetid: a642a20f-3a3c-46bc-b833-e424dab3a16d
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: CoReleaseMarshalData, CoReleaseMarshalData function [COM], _com_CoReleaseMarshalData, com.coreleasemarshaldata, combaseapi/CoReleaseMarshalData
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: combaseapi.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: REGCLS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ole32.dll
-	API-MS-Win-Core-Com-l1-1-0.dll
-	ComBase.dll
-	API-MS-Win-Core-Com-l1-1-1.dll
-	API-MS-Win-DownLevel-Ole32-l1-1-0.dll
-	API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
-	CoReleaseMarshalData
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
---

# CoReleaseMarshalData function


## -description


Destroys a previously marshaled data packet.


## -parameters




### -param pStm [in]

A  pointer to the stream that contains the data packet to be destroyed. See <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>.


## -returns



This function can return the standard return values E_FAIL, E_INVALIDARG, E_OUTOFMEMORY, and E_UNEXPECTED, as well as the following values.

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
The data packet was successfully destroyed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_E_INVALIDPOINTER</b></dt>
</dl>
</td>
<td width="60%">
An error related to the <i>pStm</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_NOTINITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/0f171cf4-87b9-43a6-97f2-80ed344fe376">CoInitialize</a> or <a href="https://msdn.microsoft.com/9a13e7a0-f2e2-466b-98f5-38d5972fa391">OleInitialize</a> function was not called on the current thread before this function was called.


</td>
</tr>
</table>
 




## -remarks



<div class="alert"><b>Important</b>  <p class="note">Security Note: Calling this method with untrusted data is a security risk. Call this method only with trusted data. For more information, see <a href="http://go.microsoft.com/fwlink/?LinkId=798821">Untrusted Data Security Risks</a>.

</div>
<div> </div>
The <b>CoReleaseMarshalData</b> function performs the following tasks:

<ol>
<li>The function reads a CLSID from the stream.</li>
<li>If COM's default marshaling implementation is being used, the function gets an <a href="https://msdn.microsoft.com/e6f08949-f27d-4aba-adff-eaf9c356a928">IMarshal</a> pointer to an instance of the standard unmarshaler. If custom marshaling is being used, the function creates a proxy by calling the <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a> function, passing the CLSID it read from the stream, and requests an <b>IMarshal</b> interface pointer to the newly created proxy.</li>
<li>Using whichever <a href="https://msdn.microsoft.com/e6f08949-f27d-4aba-adff-eaf9c356a928">IMarshal</a> interface pointer it has acquired, the function calls <a href="https://msdn.microsoft.com/c58c7768-9200-4370-930c-89a6c6d2b430">IMarshal::ReleaseMarshalData</a>.</li>
</ol>
You typically do not call this function. The only situation in which you might need to call this function is if you use custom marshaling (write and use your own implementation of <a href="https://msdn.microsoft.com/e6f08949-f27d-4aba-adff-eaf9c356a928">IMarshal</a>). Examples of when <b>CoReleaseMarshalData</b> should be called include the following situations: 

<ul>
<li>
An attempt was made to unmarshal the data packet, but it failed.

</li>
<li>
A marshaled data packet was removed from a global table.

</li>
</ul>
As an analogy, the data packet can be thought of as a reference to the original object, just as if it were another interface pointer being held on the object. Like a real interface pointer, that data packet must be released at some point. The use of <a href="https://msdn.microsoft.com/c58c7768-9200-4370-930c-89a6c6d2b430">IMarshal::ReleaseMarshalData</a> to release data packets is analogous to the use of <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> to release interface pointers.

Note that you do not need to call <b>CoReleaseMarshalData</b> after a successful call of the <a href="https://msdn.microsoft.com/d0eac0da-2f41-40c4-b756-31bc22752c17">CoUnmarshalInterface</a> function; that function releases the marshal data as part of the processing that it does.


<div class="alert"><b>Important</b>  You must call  the <b>CoReleaseMarshalData</b> function in the same apartment that called <a href="https://msdn.microsoft.com/04ca1217-eac1-43e2-b736-8d7522ce8592">CoMarshalInterface</a> to marshal the object into the stream. Failure to do this may cause the object reference held by the marshaled packet in the stream to be leaked.</div>
<div> </div>







## -see-also




<a href="https://msdn.microsoft.com/c58c7768-9200-4370-930c-89a6c6d2b430">IMarshal::ReleaseMarshalData</a>
 

 

