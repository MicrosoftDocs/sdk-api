---
UID: NF:gdiplusheaders.CustomLineCap.GetLastStatus
title: CustomLineCap::GetLastStatus (gdiplusheaders.h)
author: windows-sdk-content
description: The CustomLineCap::GetLastStatus method returns a value that indicates the nature of this CustomLineCap object's most recent method failure.
old-location: gdiplus\_gdiplus_CLASS_CustomLineCap_GetLastStatus_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\customlinecapclass\customlinecapmethods\getlaststatus_98.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CustomLineCap class [GDI+],GetLastStatus method, CustomLineCap.GetLastStatus, CustomLineCap::GetLastStatus, GetLastStatus, GetLastStatus method [GDI+], GetLastStatus method [GDI+],CustomLineCap class, _gdiplus_CLASS_CustomLineCap_GetLastStatus_, gdiplus._gdiplus_CLASS_CustomLineCap_GetLastStatus_
ms.topic: method
req.header: gdiplusheaders.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - CustomLineCap.GetLastStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# CustomLineCap::GetLastStatus


## -description


The <b>CustomLineCap::GetLastStatus</b> method returns a value that indicates the nature of this <a href="https://msdn.microsoft.com/en-us/library/ms534432(v=VS.85).aspx">CustomLineCap</a> object's most recent method failure.


## -parameters






## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

The <b>CustomLineCap::GetLastStatus</b> method returns an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.
                

If no methods invoked on this <a href="https://msdn.microsoft.com/en-us/library/ms534432(v=VS.85).aspx">CustomLineCap</a> object have failed since the previous call to <b>CustomLineCap::GetLastStatus</b>, then <b>CustomLineCap::GetLastStatus</b> returns Ok.

If at least one method invoked on this <a href="https://msdn.microsoft.com/en-us/library/ms534432(v=VS.85).aspx">CustomLineCap</a> object has failed since the previous call to <b>CustomLineCap::GetLastStatus</b>, then <b>CustomLineCap::GetLastStatus</b> returns a value that indicates the nature of the most recent failure.




## -remarks



You can call <b>CustomLineCap::GetLastStatus</b> immediately after constructing a <a href="https://msdn.microsoft.com/en-us/library/ms534432(v=VS.85).aspx">CustomLineCap</a> object to determine whether the constructor succeeded.

The first time you call the <b>CustomLineCap::GetLastStatus</b> method of a <a href="https://msdn.microsoft.com/en-us/library/ms534432(v=VS.85).aspx">CustomLineCap</a> object, it returns Ok if the constructor succeeded and all methods invoked so far on the <b>CustomLineCap</b> object succeeded. Otherwise, it returns a value that indicates the nature of the most recent failure.



