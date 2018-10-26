---
UID: NF:xenroll.IEnroll.get_UseExistingKeySet
title: IEnroll::get_UseExistingKeySet
author: windows-sdk-content
description: The UseExistingKeySet property of IEnroll4 sets or retrieves a Boolean value that determines whether the existing keys should be used.
old-location: security\ienroll4_useexistingkeyset.htm
tech.root: seccrypto
ms.assetid: 1534ec57-71d3-4189-a94e-7bcb3c0670e1
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: IEnroll interface [Security],UseExistingKeySet property, IEnroll.UseExistingKeySet, IEnroll.get_UseExistingKeySet, IEnroll::UseExistingKeySet, IEnroll::get_UseExistingKeySet, IEnroll::put_UseExistingKeySet, UseExistingKeySet property [Security], UseExistingKeySet property [Security],IEnroll interface, get_UseExistingKeySet, security.ienroll4_useexistingkeyset, xenroll/IEnroll::UseExistingKeySet, xenroll/IEnroll::get_UseExistingKeySet, xenroll/IEnroll::put_UseExistingKeySet
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: xenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - IEnroll.UseExistingKeySet
 - IEnroll.get_UseExistingKeySet
 - IEnroll.put_UseExistingKeySet
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnroll::get_UseExistingKeySet


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>UseExistingKeySet</b> property  sets or retrieves a Boolean value that determines whether the existing keys should be used.

This property was first defined in the <a href="https://msdn.microsoft.com/5be210b8-475a-4504-9cc0-5b02384e114e">IEnroll</a> interface.

This property is read/write.


## -parameters


## -remarks



 If an existing key set is used, the <b>UseExistingKeySet</b> property must be set to true.


The <b>UseExistingKeySet</b> property affects the behavior of the following methods:

<ul>
<li>
<a href="https://msdn.microsoft.com/ebbcc9ad-9f87-4abe-963b-38c57a60e45e">createPKCS10WStr</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5edd54c5-9dfb-44b8-a293-4fe6a8de45e3">createFilePKCS10WStr</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll</a>
 

 

