---
UID: NF:mfobjects.IMFAsyncResult.GetState
title: IMFAsyncResult::GetState method
author: windows-driver-content
description: Returns the state object specified by the caller in the asynchronous Begin method.
old-location: mf\imfasyncresult_getstate.htm
old-project: medfound
ms.assetid: f8ed8e71-6df7-4c94-b400-b4651a00db5b
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: GetState method [Media Foundation], GetState method [Media Foundation], IMFAsyncResult interface, GetState,IMFAsyncResult.GetState, IMFAsyncResult, IMFAsyncResult interface [Media Foundation], GetState method, IMFAsyncResult::GetState, f8ed8e71-6df7-4c94-b400-b4651a00db5b, mf.imfasyncresult_getstate, mfobjects/IMFAsyncResult::GetState
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_FILE_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFAsyncResult.GetState
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFAsyncResult::GetState method


## -description



Returns the state object specified by the caller in the asynchronous <b>Begin</b> method.




## -parameters




### -param ppunkState [out]

Receives a pointer to the state object's <b>IUnknown</b> interface. If the value is not <b>NULL</b>, the caller must release the interface.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
There is no state object associated with this asynchronous result.

</td>
</tr>
</table>
 




## -remarks



The caller of the asynchronous method specifies the state object, and can use it for any caller-defined purpose. The state object can be <b>NULL</b>. If the state object is <b>NULL</b>, <b>GetState</b> returns <b>E_POINTER</b>.

If you are implementing an asynchronous method, set the state object on the through the <i>punkState</i> parameter of the <a href="https://msdn.microsoft.com/6ff773a9-961e-4a5e-ad37-46234022c575">MFCreateAsyncResult</a> function.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/ea778eaa-6460-4a93-bd6a-1857ea8b6230">Asynchronous Callback Methods</a>



<a href="https://msdn.microsoft.com/8c95b1de-8974-445c-8070-41552ea83e53">IMFAsyncResult</a>
 

 

