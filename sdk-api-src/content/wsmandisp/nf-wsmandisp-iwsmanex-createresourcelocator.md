---
UID: NF:wsmandisp.IWSManEx.CreateResourceLocator
title: IWSManEx::CreateResourceLocator
author: windows-sdk-content
description: Creates a ResourceLocator object that can be used instead of a resource URI in Session object operations such as IWSManSession.Get, IWSManSession.Put, or Session.Enumerate.
old-location: winrm\iwsmanex_createresourcelocator.htm
tech.root: WinRM
ms.assetid: b670865d-96d6-4b06-a9a5-ed74574a0108
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CreateResourceLocator, CreateResourceLocator method [Windows Remote Management], CreateResourceLocator method [Windows Remote Management],IWSManEx interface, IWSManEx interface [Windows Remote Management],CreateResourceLocator method, IWSManEx.CreateResourceLocator, IWSManEx::CreateResourceLocator, winrm.iwsmanex_createresourcelocator, wsmandisp/IWSManEx::CreateResourceLocator
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wsmandisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WSManDisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WSManDisp.tlb
req.dll: WSMAuto.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WSMAuto.dll
api_name:
 - IWSManEx.CreateResourceLocator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wsmandisp.h
: 
- IWSManEx.CreateResourceLocator
: 
---

# IWSManEx::CreateResourceLocator


## -description


Creates a <a href="https://msdn.microsoft.com/0904b7eb-d4ce-46a7-bf58-452e7c0d41e9">ResourceLocator</a> object that can be used instead of a resource URI in <a href="https://msdn.microsoft.com/b98ca759-71cb-492e-8645-8766b202eb36">Session</a> object operations such as <a href="https://msdn.microsoft.com/f6393cfb-0787-4d30-8d02-be0996885f22">IWSManSession.Get</a>, <a href="https://msdn.microsoft.com/1224dab8-82d1-4416-8c21-e84fdda15deb">IWSManSession.Put</a>, or <a href="https://msdn.microsoft.com/b1a4815e-93aa-4a30-a67e-c52fd06c1ee1">Session.Enumerate</a>.


## -parameters




### -param strResourceLocator

TBD


### -param newResourceLocator [out]

A pointer to a new instance of <a href="https://msdn.microsoft.com/7b3dcb53-d02c-4ba6-973d-1493ba442387">IWSManResourceLocator</a>.


#### - uri [in]

The resource URI for the resource. For more information about URI strings, see <a href="https://msdn.microsoft.com/478a6e5d-0675-462e-b2fd-fd2b5379e298">Resource URIs</a>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the <b>FragmentDialect</b> property is not specified in the <a href="https://msdn.microsoft.com/7b3dcb53-d02c-4ba6-973d-1493ba442387">IWSManResourceLocator</a> object, the default is the XPath 1.0 specification. For more information, see <a href="http://go.microsoft.com/fwlink/p/?linkid=84163">http://www.w3.org/TR/xpath</a>.




## -see-also




<a href="https://msdn.microsoft.com/23fdd9d9-4a78-4c01-8e5d-c8007f39d5d6">IWSManEx</a>



<a href="https://msdn.microsoft.com/45895a4e-b7de-4469-ae78-6d1d3f9d6145">WSMan</a>



<a href="https://msdn.microsoft.com/c996f074-f14b-4edd-80b7-8f4de4cbabb0">Windows Remote Management Reference</a>
 

 

