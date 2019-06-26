---
UID: NN:unknwn.IUnknown
title: IUnknown
author: windows-sdk-content
description: Enables clients to get pointers to other interfaces on a given object through the QueryInterface method, and manage the existence of the object through the AddRef and Release methods.
old-location: com\iunknown.htm
tech.root: com
ms.assetid: 33f1d79a-33fc-4ce5-a372-e08bda378332
ms.author: windowssdkdev
ms.date: 06/05/2019
ms.keywords: IUnknown, IUnknown interface [COM], IUnknown interface [COM],described, _com_iunknown, com.iunknown, unknwn/IUnknown
ms.topic: interface
f1_keywords: 
 - "unknwn/IUnknown"
req.header: unknwn.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Unknwn.idl
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
 - Unknwn.h
api_name:
 - IUnknown
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

## -description

Enables clients to get pointers to other interfaces on a given object through the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> method, and manage the existence of the object through the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> and <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> methods. All other COM interfaces are inherited, directly or indirectly, from <b>IUnknown</b>. Therefore, the three methods in <b>IUnknown</b> are the first entries in the vtable for every interface. 

## -see-also

[Using and Implementing IUnknown](/windows/desktop/com/using-and-implementing-iunknown)
