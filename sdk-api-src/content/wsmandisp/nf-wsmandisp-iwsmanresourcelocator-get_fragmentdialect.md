---
UID: NF:wsmandisp.IWSManResourceLocator.get_FragmentDialect
title: IWSManResourceLocator::get_FragmentDialect
author: windows-sdk-content
description: Gets or sets the language dialect for a resource fragment dialect when IWSManResourceLocator is used in IWSManSession object methods such as Get, Put, or Enumerate.
old-location: winrm\iwsmanresourcelocator_fragmentdialect.htm
old-project: winrm
ms.assetid: eb458fc4-ddcc-42a2-8dd3-05498e035de2
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: FragmentDialect property [Windows Remote Management], FragmentDialect property [Windows Remote Management],IWSManResourceLocator interface, IWSManResourceLocator interface [Windows Remote Management],FragmentDialect property, IWSManResourceLocator.FragmentDialect, IWSManResourceLocator.get_FragmentDialect, IWSManResourceLocator::FragmentDialect, IWSManResourceLocator::get_FragmentDialect, IWSManResourceLocator::put_FragmentDialect, get_FragmentDialect, winrm.iwsmanresourcelocator_fragmentdialect, wsmandisp/IWSManResourceLocator::FragmentDialect, wsmandisp/IWSManResourceLocator::get_FragmentDialect, wsmandisp/IWSManResourceLocator::put_FragmentDialect
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wsmandisp.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WSManProxyAuthenticationFlags
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WSMAuto.dll
api_name:
 - IWSManResourceLocator.FragmentDialect
 - IWSManResourceLocator.get_FragmentDialect
 - IWSManResourceLocator.put_FragmentDialect
product: Windows
targetos: Windows
req.lib: WSManDisp.tlb
req.dll: WSMAuto.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSManResourceLocator::get_FragmentDialect


## -description


Gets or sets the language dialect for a <a href="https://msdn.microsoft.com/en-us/library/Aa384465(v=VS.85).aspx">resource</a> <a href="https://msdn.microsoft.com/en-us/library/Aa384465(v=VS.85).aspx">fragment</a> <i>dialect</i> when <a href="https://msdn.microsoft.com/7b3dcb53-d02c-4ba6-973d-1493ba442387">IWSManResourceLocator</a> is used in <a href="https://msdn.microsoft.com/3e016080-339f-4bda-bfd2-f912e090981f">IWSManSession</a> object methods such as <a href="https://msdn.microsoft.com/f6393cfb-0787-4d30-8d02-be0996885f22">Get</a>, <a href="https://msdn.microsoft.com/1224dab8-82d1-4416-8c21-e84fdda15deb">Put</a>, or <a href="https://msdn.microsoft.com/b1a4815e-93aa-4a30-a67e-c52fd06c1ee1">Enumerate</a>. A fragment represents one property or part of a resource. You can provide an <a href="https://msdn.microsoft.com/7b3dcb53-d02c-4ba6-973d-1493ba442387">IWSManResourceLocator</a> object instead of specifying a <a href="https://msdn.microsoft.com/en-us/library/Aa384465(v=VS.85).aspx">resource URI</a> in <a href="https://msdn.microsoft.com/3e016080-339f-4bda-bfd2-f912e090981f">IWSManSession</a> object operations. 

This property is read/write.


## -parameters


## -remarks



The dialect string defaults to the XPath 1.0 specification. For more information, see <a href="http://go.microsoft.com/fwlink/p/?linkid=84163">http://www.w3.org/TR/xpath</a>.




## -see-also




<a href="https://msdn.microsoft.com/7b3dcb53-d02c-4ba6-973d-1493ba442387">IWSManResourceLocator</a>



<a href="https://msdn.microsoft.com/60b08084-f4b9-4049-b0cd-a7420fcffd7c">ResourceLocator.FragmentDialect</a>
 

 

