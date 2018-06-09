---
UID: NF:strmif.IDvdControl.ButtonSelectAndActivate
title: IDvdControl::ButtonSelectAndActivate
author: windows-sdk-content
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Selects and activates the specified button.
old-location: dshow\idvdcontrol_buttonselectandactivate.htm
old-project: DirectShow
ms.assetid: 15ed6a4e-d798-49c9-bff3-c77207658d31
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: ButtonSelectAndActivate, ButtonSelectAndActivate method [DirectShow], ButtonSelectAndActivate method [DirectShow],IDvdControl interface, IDvdControl interface [DirectShow],ButtonSelectAndActivate method, IDvdControl.ButtonSelectAndActivate, IDvdControl::ButtonSelectAndActivate, IDvdControlButtonSelectAndActivate, dshow.idvdcontrol_buttonselectandactivate, strmif/IDvdControl::ButtonSelectAndActivate
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IDvdControl.ButtonSelectAndActivate
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDvdControl::ButtonSelectAndActivate


## -description



<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="https://msdn.microsoft.com/eda43b20-1c4d-4769-bb87-3942716af13c">IDvdControl2</a> instread.</div>
<div> </div>
Selects and activates the specified button.




## -parameters




### -param ulButton






#### - uiButton [in]

Value that specifies the button that will be selected and activated, which must be from 1 through 36.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



Electronic remote control devices typically have a number of buttons that activate various functions of a DVD playback unit. Typically, you call this method when a user clicks a button on the control device; DirectShow then indicates that the button was selected (by playing a sound or changing a graphic, for example) and calls methods appropriate to which button was selected, such as <a href="https://msdn.microsoft.com/6a5ee6ed-2baa-45d6-a874-5df4e5c56841">ButtonActivate</a>.

This method returns an error unless the domain is DVD_DOMAIN_VideoManagerMenu, DVD_DOMAIN_VideoTitleSetMenu, or DVD_DOMAIN_Title. For more information, see <a href="https://msdn.microsoft.com/2763a159-d4de-44c2-905b-5828f328cbd2">DVD_DOMAIN</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/a6ca0fe8-84e3-43e6-9421-29dcff056dfd">IDvdControl Interface</a>
 

 

