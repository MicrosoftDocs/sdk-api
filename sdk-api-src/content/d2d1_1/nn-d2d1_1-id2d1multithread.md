---
UID: NN:d2d1_1.ID2D1Multithread
title: ID2D1Multithread (d2d1_1.h)
description: A locking mechanism from a Direct2D factory that Direct2D uses to control exclusive resource access in an app that is uses multiple threads.
helpviewer_keywords: ["ID2D1Multithread","ID2D1Multithread interface [Direct2D]","ID2D1Multithread interface [Direct2D]","described","d2d1_1/ID2D1Multithread","direct2d.id2d1multithread"]
old-location: direct2d\id2d1multithread.htm
tech.root: Direct2D
ms.assetid: 885E7580-6BF0-4A44-9493-6D4FFCB5577B
ms.date: 12/05/2018
ms.keywords: ID2D1Multithread, ID2D1Multithread interface [Direct2D], ID2D1Multithread interface [Direct2D],described, d2d1_1/ID2D1Multithread, direct2d.id2d1multithread
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1Multithread
 - d2d1_1/ID2D1Multithread
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1Multithread
---

# ID2D1Multithread interface


## -description

A  locking mechanism from a <a href="https://docs.microsoft.com/windows/desktop/Direct2D/direct2d-portal">Direct2D</a> factory that Direct2D 
          uses to control exclusive resource access in an app that is uses multiple threads.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1Multithread</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID2D1Multithread</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1Multithread</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1multithread-enter">Enter</a>
</td>
<td align="left" width="63%">
Enters the Direct2D API critical section, if it exists. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1multithread-getmultithreadprotected">GetMultithreadProtected</a>
</td>
<td align="left" width="63%">
Returns whether the Direct2D factory was created with the <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/ne-d2d1-d2d1_factory_type">D2D1_FACTORY_TYPE_MULTI_THREADED</a> flag.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1multithread-leave">Leave</a>
</td>
<td align="left" width="63%">
Leaves the Direct2D API critical section, if it exists.

</td>
</tr>
</table>

## -remarks

You can get an <b>ID2D1Multithread</b> object by querying for it from an <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1factory">ID2D1Factory</a> 
        object.
      

You should use this lock while doing any operation on a Direct3D/DXGI surface. <a href="https://docs.microsoft.com/windows/desktop/Direct2D/direct2d-portal">Direct2D</a> will wait on any call until you 
        leave the critical section.
      

<div class="alert"><b>Note</b>  Normal rendering is guarded automatically by an internal <a href="https://docs.microsoft.com/windows/desktop/Direct2D/direct2d-portal">Direct2D</a> lock.
        </div>
<div> </div>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1factory">ID2D1Factory</a>

