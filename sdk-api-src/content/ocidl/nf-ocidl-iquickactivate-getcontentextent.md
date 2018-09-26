---
UID: NF:ocidl.IQuickActivate.GetContentExtent
title: IQuickActivate::GetContentExtent
author: windows-sdk-content
description: Gets the content extent of a control.
old-location: com\iquickactivate_getcontentextent.htm
tech.root: com
ms.assetid: ead9bf4d-44a1-4237-ad03-28a4253819b8
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: GetContentExtent, GetContentExtent method [COM], GetContentExtent method [COM],IQuickActivate interface, IQuickActivate interface [COM],GetContentExtent method, IQuickActivate.GetContentExtent, IQuickActivate::GetContentExtent, _ctrl_iquickactivate_getcontentextent, com.iquickactivate_getcontentextent, ocidl/IQuickActivate::GetContentExtent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - IQuickActivate.GetContentExtent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IQuickActivate::GetContentExtent


## -description


Gets the content extent of a control.


## -parameters




### -param pSizel [out]

A pointer to a structure that contains size of the content extent.


## -returns



If the method succeeds, the return value is S_OK. Otherwise, it is E_FAIL.




## -remarks



The <b>SIZEL</b> structure is defined in Wtypes.h as follows.

<pre class="syntax" xml:space="preserve"><code>typedef struct tagSIZEL
    {
    LONG cx;
    LONG cy;
    } 	SIZEL;

typedef struct tagSIZEL *PSIZEL;

typedef struct tagSIZEL *LPSIZEL;</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/9b3e3b56-5055-4dfa-83e6-702578662463">IQuickActivate</a>
 

 

