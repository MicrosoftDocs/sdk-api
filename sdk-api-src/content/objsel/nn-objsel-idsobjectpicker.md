---
UID: NN:objsel.IDsObjectPicker
title: IDsObjectPicker
author: windows-sdk-content
description: The IDsObjectPicker interface is used by an application to initialize and display an object picker dialog box. To create an instance of this interface, call CoCreateInstance with the CLSID_DsObjectPicker class identifier as shown below.
old-location: ad\idsobjectpicker.htm
tech.root: ad
ms.assetid: f2f9da7d-7a09-4b49-a750-078a4573e213
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: IDsObjectPicker, IDsObjectPicker interface [Active Directory], IDsObjectPicker interface [Active Directory],described, _glines_idsobjectpicker, ad.idsobjectpicker, objsel/IDsObjectPicker
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: objsel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: Objsel.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Objsel.dll
api_name:
 - IDsObjectPicker
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDsObjectPicker interface


## -description


The <b>IDsObjectPicker</b> interface is used by an application to initialize and display an object picker dialog box. To create an  instance of this interface, call <a href="https://msdn.microsoft.com/en-us/library/ms686615(v=VS.85).aspx">CoCreateInstance</a> with the <b>CLSID_DsObjectPicker</b> class identifier as shown below.

```cpp
HRESULT hr = S_OK;
IDsObjectPicker *pDsObjectPicker = NULL;
 
hr = CoCreateInstance(CLSID_DsObjectPicker,
             NULL,
             CLSCTX_INPROC_SERVER,
             IID_IDsObjectPicker,
             (void **) &pDsObjectPicker);
```

The  <b>IDsObjectPicker</b> implemented by the system  supports both apartment and free-threading models and is thread safe. In practice, this means that a call to the methods of this interface will block until no other thread of your application is calling any other method on that instance of the interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDsObjectPicker</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDsObjectPicker</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDsObjectPicker</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bcf4d283-6709-4425-a122-8f0808502b58">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the interface with data about the scopes, filters, and options used by the dialog box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/76192a35-10e1-46e3-8724-7637d47d8eca">InvokeDialog</a>
</td>
<td align="left" width="63%">
Displays the dialog box and returns the user's selections.

</td>
</tr>
</table> 


## -remarks



It is acceptable to create and initialize a single instance of the <b>IDsObjectPicker</b> interface and then make multiple 
calls to <a href="https://msdn.microsoft.com/76192a35-10e1-46e3-8724-7637d47d8eca">InvokeDialog</a> without having to reinitializing the interface.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms686615(v=VS.85).aspx">CoCreateInstance</a>



<a href="https://msdn.microsoft.com/5b3e5d71-afd2-49db-b3a2-f9a49f0b2b3a">Directory Object Picker</a>
 

 

