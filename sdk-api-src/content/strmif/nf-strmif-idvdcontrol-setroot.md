---
UID: NF:strmif.IDvdControl.SetRoot
title: IDvdControl::SetRoot method
author: windows-driver-content
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Sets the root directory containing the DVD-Video volume.
old-location: dshow\idvdcontrol_setroot.htm
old-project: DirectShow
ms.assetid: 3068edc0-c052-4f44-9f62-453320af20a3
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IDvdControl, IDvdControl interface [DirectShow], SetRoot method, IDvdControl::SetRoot, IDvdControlSetRoot, SetRoot method [DirectShow], SetRoot method [DirectShow], IDvdControl interface, SetRoot,IDvdControl.SetRoot, dshow.idvdcontrol_setroot, strmif/IDvdControl::SetRoot
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmif.h
api_name:
-	IDvdControl.SetRoot
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDvdControl::SetRoot method


## -description



<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="https://msdn.microsoft.com/eda43b20-1c4d-4769-bb87-3942716af13c">IDvdControl2</a> instread.</div>
<div> </div>
Sets the root directory containing the DVD-Video volume.




## -parameters




### -param pszPath [in]

Pointer to the directory name to set as the root directory.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



This method returns an error unless the domain is DVD_DOMAIN_Stop. For more information, see <a href="https://msdn.microsoft.com/2763a159-d4de-44c2-905b-5828f328cbd2">DVD_DOMAIN</a>.

If you haven't set the root directory before calling <a href="https://msdn.microsoft.com/5ca710f0-8f08-43d6-8cc1-a25068d5e0ef">IDvdControl::TitlePlay</a>, the first drive starting from C: that contains a VIDEO_TS directory in the top level directory will be used as the root.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/a6ca0fe8-84e3-43e6-9421-29dcff056dfd">IDvdControl Interface</a>
 

 

