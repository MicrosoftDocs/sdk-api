---
UID: NF:tom.ITextFont2.SetCharRep
title: ITextFont2::SetCharRep
author: windows-driver-content
description: Sets the character repertoire (writing system).
old-location: controls\itextfont2_setcharrep.htm
old-project: Controls
ms.assetid: 6c57b5e5-a5c7-416a-851c-fc8ef16b5a9a
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: ITextFont2 interface [Windows Controls],SetCharRep method, ITextFont2.SetCharRep, ITextFont2::SetCharRep, SetCharRep, SetCharRep method [Windows Controls], SetCharRep method [Windows Controls],ITextFont2 interface, controls.itextfont2_setcharrep, tom/ITextFont2::SetCharRep
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MANCODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msftedit.dll
api_name:
-	ITextFont2.SetCharRep
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextFont2::SetCharRep


## -description


Sets the character repertoire (writing system).


## -parameters




### -param Value [in]

Type: <b>long</b>

The new character repertoire. For a list of possible values, see <a href="https://msdn.microsoft.com/250b9fe9-8f63-4f6f-9b14-d6fdac3580b0">ITextFont2::GetCharRep</a>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d2d43bfd-7cdf-458a-822d-e3965bfe2284">ITextFont2</a>



<a href="https://msdn.microsoft.com/250b9fe9-8f63-4f6f-9b14-d6fdac3580b0">ITextFont2::GetCharRep</a>
 

 

