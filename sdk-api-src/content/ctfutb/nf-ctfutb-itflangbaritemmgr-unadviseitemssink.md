---
UID: NF:ctfutb.ITfLangBarItemMgr.UnadviseItemsSink
title: ITfLangBarItemMgr::UnadviseItemsSink (ctfutb.h)
author: windows-sdk-content
description: ITfLangBarItemMgr::UnadviseItemsSink method
old-location: tsf\itflangbaritemmgr_unadviseitemssink.htm
tech.root: TSF
ms.assetid: e15fb870-bedc-412d-9561-4db6c0515799
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITfLangBarItemMgr interface [Text Services Framework],UnadviseItemsSink method, ITfLangBarItemMgr.UnadviseItemsSink, ITfLangBarItemMgr::UnadviseItemsSink, UnadviseItemsSink, UnadviseItemsSink method [Text Services Framework], UnadviseItemsSink method [Text Services Framework],ITfLangBarItemMgr interface, _tsf_itflangbaritemmgr_unadviseitemssink_ref, ctfutb/ITfLangBarItemMgr::UnadviseItemsSink, tsf.itflangbaritemmgr_unadviseitemssink
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
ms.custom: 19H1
---

# ITfLangBarItemMgr::UnadviseItemsSink


## -description




## -parameters




### -param ulCount [in]

Contains the number of advise sinks to install.


### -param pdwCookie [in]

Pointer to an array of <b>DWORD</b>s that identify the advise sinks to remove. These cookies are obtained when the advise sinks are installed with <a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-adviseitemsink">ITfLangBarItemMgr::AdviseItemSink</a> or <a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-adviseitemssink">ITfLangBarItemMgr::AdviseItemsSink</a>. This array must be at least <i>ulCount</i> elements in length.


## -returns



This method has no return values.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritemmgr">ITfLangBarItemMgr</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-adviseitemsink">ITfLangBarItemMgr::AdviseItemSink
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-adviseitemssink">ITfLangBarItemMgr::AdviseItemsSink
      </a>
 

 

