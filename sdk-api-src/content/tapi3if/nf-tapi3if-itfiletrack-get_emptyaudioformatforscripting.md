---
UID: NF:tapi3if.ITFileTrack.get_EmptyAudioFormatForScripting
title: ITFileTrack::get_EmptyAudioFormatForScripting
author: windows-sdk-content
description: The get_EmptyAudioFormatForScripting method is used to get an ITScriptableAudioFormat interface with all fields set to 0.
old-location: tapi3\itfiletrack_get_emptyaudioformatforscripting.htm
old-project: Tapi
ms.assetid: 80644b51-4b04-4299-a486-284e77583feb
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: ITFileTrack interface [TAPI 2.2],get_EmptyAudioFormatForScripting method, ITFileTrack.get_EmptyAudioFormatForScripting, ITFileTrack::get_EmptyAudioFormatForScripting, _tapi3_itfiletrack_get_emptyaudioformatforscripting, get_EmptyAudioFormatForScripting, get_EmptyAudioFormatForScripting method [TAPI 2.2], get_EmptyAudioFormatForScripting method [TAPI 2.2],ITFileTrack interface, tapi3.itfiletrack_get_emptyaudioformatforscripting, tapi3if/ITFileTrack::get_EmptyAudioFormatForScripting
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: TERMINAL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Tapi3.dll
api_name:
-	ITFileTrack.get_EmptyAudioFormatForScripting
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITFileTrack::get_EmptyAudioFormatForScripting


## -description


The 
<b>get_EmptyAudioFormatForScripting</b> method is used to get an 
<a href="https://msdn.microsoft.com/6b5d069a-044f-4bd4-b661-6100a2607107">ITScriptableAudioFormat</a> interface with all fields set to 0.


## -parameters




### -param ppAudioFormat [out]

Pointer to 
<a href="https://msdn.microsoft.com/6b5d069a-044f-4bd4-b661-6100a2607107">ITScriptableAudioFormat</a> interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/6b5d069a-044f-4bd4-b661-6100a2607107">ITScriptableAudioFormat</a> interface returned by <b>ITFileTrack::get_EmptyAudioFormatForScripting</b>. The application must call <b>Release</b> on 
<b>ITScriptableAudioFormat</b> to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/590ca1ea-e058-4238-b01c-249fddd3c87d">ITFileTrack</a>
 

 

