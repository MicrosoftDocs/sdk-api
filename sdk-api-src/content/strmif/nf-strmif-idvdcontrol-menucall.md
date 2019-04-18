---
UID: NF:strmif.IDvdControl.MenuCall
title: IDvdControl::MenuCall (strmif.h)
author: windows-sdk-content
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Displays the specified menu on the screen.
old-location: dshow\idvdcontrol_menucall.htm
tech.root: DirectShow
ms.assetid: b0e27b7a-cf14-4b4c-849e-0fa7f6b1c0ed
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDvdControl interface [DirectShow],MenuCall method, IDvdControl.MenuCall, IDvdControl::MenuCall, IDvdControlMenuCall, MenuCall, MenuCall method [DirectShow], MenuCall method [DirectShow],IDvdControl interface, dshow.idvdcontrol_menucall, strmif/IDvdControl::MenuCall
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IDvdControl.MenuCall
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvdControl::MenuCall


## -description



<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="https://msdn.microsoft.com/eda43b20-1c4d-4769-bb87-3942716af13c">IDvdControl2</a> instread.</div>
<div> </div>
Displays the specified menu on the screen.




## -parameters




### -param MenuID [in]

Value that specifies the menu to display. Member of the <a href="https://msdn.microsoft.com/2fd107d7-7531-4bce-89b9-b44388b47b91">DVD_MENU_ID</a> enumerated data type.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



This method returns an error unless the domain is DVD_DOMAIN_VideoManagerMenu, DVD_DOMAIN_VideoTitleSetMenu, DVD_DOMAIN_Title, or DVD_DOMAIN_Stop. For more information, see <a href="https://msdn.microsoft.com/2763a159-d4de-44c2-905b-5828f328cbd2">DVD_DOMAIN</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/a6ca0fe8-84e3-43e6-9421-29dcff056dfd">IDvdControl Interface</a>
 

 

