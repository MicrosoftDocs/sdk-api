---
UID: NF:windowsstoragecom.IRandomAccessStreamFileAccessMode.GetMode
title: IRandomAccessStreamFileAccessMode::GetMode method
author: windows-driver-content
description: Retrieves the file access mode that was used when the StorageFile.OpenAsync method was called to open the random-access byte stream.
old-location: winrt\irandomaccessstreamfileaccessmode_getmode.htm
old-project: WinRT
ms.assetid: F542C4E4-5B65-4909-AF08-C129297A1085
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: GetMode method [Windows Runtime], GetMode method [Windows Runtime], IRandomAccessStreamFileAccessMode interface, GetMode,IRandomAccessStreamFileAccessMode.GetMode, IRandomAccessStreamFileAccessMode, IRandomAccessStreamFileAccessMode interface [Windows Runtime], GetMode method, IRandomAccessStreamFileAccessMode::GetMode, windowsstoragecom/IRandomAccessStreamFileAccessMode::GetMode, winrt.irandomaccessstreamfileaccessmode_getmode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: windowsstoragecom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: HANDLE_SHARING_OPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	windows.storage.dll
api_name:
-	IRandomAccessStreamFileAccessMode.GetMode
product: Windows
targetos: Windows
req.lib: 
req.dll: Windows.storage.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IRandomAccessStreamFileAccessMode::GetMode method


## -description


Retrieves the file access mode that was used when the <a href="https://msdn.microsoft.com/128318b6-ddfb-44d0-9fcb-80410ad284bf">StorageFile.OpenAsync</a> method was called to open the random-access byte stream.


## -parameters




### -param fileAccessMode [out]

The file access mode that was used when the <a href="https://msdn.microsoft.com/128318b6-ddfb-44d0-9fcb-80410ad284bf">StorageFile.OpenAsync</a> method was called to open the random-access byte stream. Cast this value as a <a href="https://msdn.microsoft.com/2905de68-84f9-4cc1-9389-8ec611b1eece">Windows::Storage::FileAccessMode</a> enumeration value.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/20A538B5-ACD6-4BD9-9CDC-3F2CCDCAF251">IRandomAccessStreamFileAccessMode</a>



<a href="https://msdn.microsoft.com/128318b6-ddfb-44d0-9fcb-80410ad284bf">StorageFile.OpenAsync</a>



<a href="https://msdn.microsoft.com/2905de68-84f9-4cc1-9389-8ec611b1eece">Windows::Storage::FileAccessMode</a>
 

 

