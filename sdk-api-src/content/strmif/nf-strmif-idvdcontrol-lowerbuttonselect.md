---
UID: NF:strmif.IDvdControl.LowerButtonSelect
title: IDvdControl::LowerButtonSelect (strmif.h)
author: windows-sdk-content
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Selects the lower directional button from the displayed menu.
old-location: dshow\idvdcontrol_lowerbuttonselect.htm
tech.root: DirectShow
ms.assetid: eba476a5-c949-4ce1-b296-314e36afc912
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDvdControl interface [DirectShow],LowerButtonSelect method, IDvdControl.LowerButtonSelect, IDvdControl::LowerButtonSelect, IDvdControlLowerButtonSelect, LowerButtonSelect, LowerButtonSelect method [DirectShow], LowerButtonSelect method [DirectShow],IDvdControl interface, dshow.idvdcontrol_lowerbuttonselect, strmif/IDvdControl::LowerButtonSelect
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
 - IDvdControl.LowerButtonSelect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvdControl::LowerButtonSelect


## -description



<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="https://msdn.microsoft.com/eda43b20-1c4d-4769-bb87-3942716af13c">IDvdControl2</a> instread.</div>
<div> </div>
Selects the lower directional button from the displayed menu.




## -parameters






## -returns



Returns an <b>HRESULT</b> value.




## -remarks



On physical or electronic remote control devices, there is often a group of four directional buttons used for certain types of operations (such as menu navigation). This method tells DirectShow that something (the user, probably) triggered the lower directional button.

Selecting a DVD button simply highlights the button but does not activate the button. Selecting is the Windows equivalent of tabbing to a button but not pressing the SPACEBAR or ENTER key. Activating is the Windows equivalent of pressing the SPACEBAR or ENTER key after tabbing to a button.

This method returns an error unless the domain is DVD_DOMAIN_VideoManagerMenu, DVD_DOMAIN_VideoTitleSetMenu, or DVD_DOMAIN_Title. For more information, see <a href="https://msdn.microsoft.com/2763a159-d4de-44c2-905b-5828f328cbd2">DVD_DOMAIN</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/a6ca0fe8-84e3-43e6-9421-29dcff056dfd">IDvdControl Interface</a>
 

 

