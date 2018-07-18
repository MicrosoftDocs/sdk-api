---
UID: NF:mfapi.MFCancelWorkItem
title: MFCancelWorkItem function
author: windows-sdk-content
description: Attempts to cancel an asynchronous operation that was scheduled with MFScheduleWorkItem or MFScheduleWorkItemEx.
old-location: mf\mfcancelworkitem.htm
old-project: medfound
ms.assetid: a24fae61-30c8-4aca-b067-22b99f904fd8
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: MFCancelWorkItem, MFCancelWorkItem function [Media Foundation], a24fae61-30c8-4aca-b067-22b99f904fd8, mf.mfcancelworkitem, mfapi/MFCancelWorkItem
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MF_CUSTOM_DECODE_UNIT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFCancelWorkItem
product: Windows
targetos: Windows
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFCancelWorkItem function


## -description



          Attempts to cancel an asynchronous operation that was scheduled with <a href="https://msdn.microsoft.com/c14786e4-7fbe-4748-a6ba-e9e68f78b241">MFScheduleWorkItem</a> or <a href="https://msdn.microsoft.com/b698cae1-4f3b-4649-b6f7-583f223eb90c">MFScheduleWorkItemEx</a>.


## -parameters




### -param Key [in]


            The key that was received in the <i>pKey</i> parameter of the <a href="https://msdn.microsoft.com/c14786e4-7fbe-4748-a6ba-e9e68f78b241">MFScheduleWorkItem</a>, <a href="https://msdn.microsoft.com/b698cae1-4f3b-4649-b6f7-583f223eb90c">MFScheduleWorkItemEx</a>, or <a href="https://msdn.microsoft.com/BBD80C60-E42F-4B3B-96E3-E01058A27DB8">MFPutWaitingWorkItem</a> functions.
          


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Because work items are asynchronous, the  work-item callback might still be invoked after <b>MFCancelWorkItem</b> is called.

This function is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/f886d096-b1f5-42e4-8888-501b58bffd50">Work Queues</a>
 

 

