---
UID: NF:ctfutb.ITfLangBarItemMgr.UnadviseItemsSink
title: ITfLangBarItemMgr::UnadviseItemsSink
author: windows-sdk-content
description: ITfLangBarItemMgr::UnadviseItemsSink method
old-location: tsf\itflangbaritemmgr_unadviseitemssink.htm
tech.root: TSF
ms.assetid: e15fb870-bedc-412d-9561-4db6c0515799
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ITfLangBarItemMgr interface [Text Services Framework],UnadviseItemsSink method, ITfLangBarItemMgr.UnadviseItemsSink, ITfLangBarItemMgr::UnadviseItemsSink, UnadviseItemsSink, UnadviseItemsSink method [Text Services Framework], UnadviseItemsSink method [Text Services Framework],ITfLangBarItemMgr interface, _tsf_itflangbaritemmgr_unadviseitemssink_ref, ctfutb/ITfLangBarItemMgr::UnadviseItemsSink, tsf.itflangbaritemmgr_unadviseitemssink
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ctfutb.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctfutb.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfLangBarItemMgr.UnadviseItemsSink
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfLangBarItemMgr::UnadviseItemsSink


## -description




## -parameters




### -param ulCount [in]

Contains the number of advise sinks to install.


### -param pdwCookie [in]

Pointer to an array of <b>DWORD</b>s that identify the advise sinks to remove. These cookies are obtained when the advise sinks are installed with <a href="https://msdn.microsoft.com/en-us/library/ms628725(v=VS.85).aspx">ITfLangBarItemMgr::AdviseItemSink</a> or <a href="https://msdn.microsoft.com/en-us/library/ms628726(v=VS.85).aspx">ITfLangBarItemMgr::AdviseItemsSink</a>. This array must be at least <i>ulCount</i> elements in length.


## -returns



This method has no return values.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms628723(v=VS.85).aspx">ITfLangBarItemMgr</a>



<a href="https://msdn.microsoft.com/c01d80eb-9156-4fbf-98ff-7f06b145e72f">ITfLangBarItemMgr::AdviseItemSink
      </a>



<a href="https://msdn.microsoft.com/c0a3e86b-487b-410a-8bba-c2b5126126d2">ITfLangBarItemMgr::AdviseItemsSink
      </a>
 

 

