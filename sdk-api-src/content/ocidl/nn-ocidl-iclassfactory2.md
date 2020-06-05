---
UID: NN:ocidl.IClassFactory2
title: IClassFactory2 (ocidl.h)
description: Enables a class factory object, in any sort of object server, to control object creation through licensing.helpviewer_keywords: ["IClassFactory2","IClassFactory2 interface [COM]","IClassFactory2 interface [COM]","described","_com_iclassfactory2","com.iclassfactory2","ocidl/IClassFactory2"]
old-location: com\iclassfactory2.htm
tech.root: com
ms.assetid: c49c7612-3b1f-4535-baf3-8458b3f34f95
ms.date: 12/05/2018
ms.keywords: IClassFactory2, IClassFactory2 interface [COM], IClassFactory2 interface [COM],described, _com_iclassfactory2, com.iclassfactory2, ocidl/IClassFactory2
f1_keywords:
- ocidl/IClassFactory2
dev_langs:
- c++
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- OCIdl.h
api_name:
- IClassFactory2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IClassFactory2 interface


## -description


Enables a class factory object, in any sort of object server, to control object creation through licensing. 

This interface is an extension to <a href="https://docs.microsoft.com/windows/desktop/api/unknwnbase/nn-unknwnbase-iclassfactory">IClassFactory</a>. This extension enables a class factory executing on a licensed machine to provide a license key that can be used later to create an object instance on an unlicensed machine. Such considerations are important for objects like controls that are used to build applications on a licensed machine. Subsequently, the application built must be able to run on an unlicensed machine. The license key gives only that one client application the right to instantiate objects through <b>IClassFactory2</b> when a full machine license does not exist.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IClassFactory2</b> interface inherits from <b>IClassFactory</b>. <b>IClassFactory2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IClassFactory2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-iclassfactory2-createinstancelic">CreateInstanceLic</a>
</td>
<td align="left" width="63%">
Creates an instance of the licensed object for the specified license key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-iclassfactory2-getlicinfo">GetLicInfo</a>
</td>
<td align="left" width="63%">
Retrieves information about the licensing capabilities of this class factory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-iclassfactory2-requestlickey">RequestLicKey</a>
</td>
<td align="left" width="63%">
Creates a license key that the caller can save and use later to create an instance of the licensed object.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/unknwnbase/nn-unknwnbase-iclassfactory">IClassFactory</a>
 

 

