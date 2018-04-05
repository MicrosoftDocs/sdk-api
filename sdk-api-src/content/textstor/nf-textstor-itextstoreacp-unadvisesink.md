---
UID: NF:textstor.ITextStoreACP.UnadviseSink
title: ITextStoreACP::UnadviseSink method
author: windows-driver-content
description: The ITextStoreACP::UnadviseSink method is called by an application to indicate that it no longer requires notifications from the TSF manager. The TSF manager will release the sink interface and stop notifications.
old-location: tsf\itextstoreacp_unadvisesink.htm
old-project: TSF
ms.assetid: 11445652-e349-46a4-8887-1d1127e16275
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: ITextStoreACP, ITextStoreACP interface [Text Services Framework], UnadviseSink method, ITextStoreACP::UnadviseSink, UnadviseSink method [Text Services Framework], UnadviseSink method [Text Services Framework], ITextStoreACP interface, UnadviseSink,ITextStoreACP.UnadviseSink, _tsf_itextstoreacp_unadvisesink_ref, textstor/ITextStoreACP::UnadviseSink, tsf.itextstoreacp_unadvisesink
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TsRunType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msctf.dll
api_name:
-	ITextStoreACP.UnadviseSink
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextStoreACP::UnadviseSink method


## -description


The <b>ITextStoreACP::UnadviseSink</b> method is called by an application to indicate that it no longer requires notifications from the TSF manager. The TSF manager will release the sink interface and stop notifications.


## -parameters




### -param punk [in]

Pointer to a sink object. Cannot be <b>NULL</b>.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CONNECT_E_NOCONNECTION</b></dt>
</dl>
</td>
<td width="60%">
There is no active sink object.

</td>
</tr>
</table>
 




## -remarks



Every call to the <a href="https://msdn.microsoft.com/a2196d1c-b03e-44b4-b695-970feddb8ce5">ITextStoreAnchor::AdviseSink</a> method, which registers a new sink object, should be matched by a call to this method. Calls to the <b>ITextStoreAnchor::AdviseSink</b> method that only update the <i>dwMask</i> parameter of a sink which was previously registered, do not require a call to the <a href="https://msdn.microsoft.com/01ddc659-0ed9-41e9-bde9-92aad9d74716">ITextStoreAnchor::UnadviseSink</a> method.

For example, to register a sink object, an application calls the <b>ITextStoreAnchor::AdviseSink</b> method the first time. After registering the sink object, the application can call the <b>ITextStoreAnchor::AdviseSink</b> method again with the same sink object to change the <i>dwMask</i> parameter. To unregister the sink object, an application calls the <b>ITextStoreAnchor::UnadviseSink</b> method.

The <i>punk</i> parameter must have the same COM identity as the pointer originally passed in the <b>ITextStoreAnchor::AdviseSink</b> method.




## -see-also




<a href="https://msdn.microsoft.com/21e011f7-6791-4eb9-85c9-18bd10107119">ITextStoreACP</a>



<a href="https://msdn.microsoft.com/aadf54e4-25ba-4280-a184-e1d2a2594c3c">ITextStoreACP::AdviseSink
      </a>
 

 

