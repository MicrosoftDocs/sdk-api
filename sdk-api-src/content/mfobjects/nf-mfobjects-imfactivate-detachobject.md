---
UID: NF:mfobjects.IMFActivate.DetachObject
title: IMFActivate::DetachObject (mfobjects.h)
author: windows-sdk-content
description: Detaches the created object from the activation object.
old-location: mf\imfactivate_detachobject.htm
tech.root: medfound
ms.assetid: 15216c57-f85d-4087-ad52-d35059647828
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 15216c57-f85d-4087-ad52-d35059647828, DetachObject, DetachObject method [Media Foundation], DetachObject method [Media Foundation],IMFActivate interface, IMFActivate interface [Media Foundation],DetachObject method, IMFActivate.DetachObject, IMFActivate::DetachObject, mf.imfactivate_detachobject, mfobjects/IMFActivate::DetachObject
ms.topic: method
f1_keywords: ["mfobjects/IMFActivate.DetachObject"]
req.header: mfobjects.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFActivate.DetachObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFActivate::DetachObject


## -description



Detaches the created object from the activation object.




## -parameters






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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

</td>
</tr>
</table>
 




## -remarks



The activation object releases all of its internal references to the created object. If you call <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject">ActivateObject</a> again, the activation object will create a new instance of the other object.

The <b>DetachObject</b> method does not shut down the created object. If the <b>DetachObject</b> method succeeds, the client must shut down the created object. This rule applies only to objects that have a shutdown method or that support the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfshutdown">IMFShutdown</a> interface. See the remarks for <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject">IMFActivate::ActivateObject</a>.

Implementation of this method is optional. If the activation object does not support this method, the method returns E_NOTIMPL.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/activation-objects">Activation Objects</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a>
 

 

