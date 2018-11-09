---
UID: NF:strmif.IDvdControl.ButtonActivate
title: IDvdControl::ButtonActivate
author: windows-sdk-content
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Activates the selected button.
old-location: dshow\idvdcontrol_buttonactivate.htm
tech.root: DirectShow
ms.assetid: 6a5ee6ed-2baa-45d6-a874-5df4e5c56841
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ButtonActivate, ButtonActivate method [DirectShow], ButtonActivate method [DirectShow],IDvdControl interface, IDvdControl interface [DirectShow],ButtonActivate method, IDvdControl.ButtonActivate, IDvdControl::ButtonActivate, IDvdControlButtonActivate, dshow.idvdcontrol_buttonactivate, strmif/IDvdControl::ButtonActivate
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
 - IDvdControl.ButtonActivate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvdControl::ButtonActivate


## -description



<div class="alert"><b>Note</b>  The <a href="https://msdn.microsoft.com/a6ca0fe8-84e3-43e6-9421-29dcff056dfd">IDvdControl</a> interface is deprecated. Use <a href="https://msdn.microsoft.com/eda43b20-1c4d-4769-bb87-3942716af13c">IDvdControl2</a> instread.</div>
<div> </div>
Activates the selected button.




## -parameters






## -returns



This method does not return a value.




## -remarks



Selecting a DVD button simply highlights the button but does not activate the button. Selecting is equivalent of tabbing to a button but not pressing the SPACEBAR or ENTER key. Activating is equivalent of pressing the SPACEBAR or ENTER key after tabbing to a button.

This method returns an error unless the domain is DVD_DOMAIN_VideoManagerMenu, DVD_DOMAIN_VideoTitleSetMenu, or DVD_DOMAIN_Title. For more information, see <a href="https://msdn.microsoft.com/2763a159-d4de-44c2-905b-5828f328cbd2">DVD_DOMAIN</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/a6ca0fe8-84e3-43e6-9421-29dcff056dfd">IDvdControl Interface</a>



<a href="https://msdn.microsoft.com/15ed6a4e-d798-49c9-bff3-c77207658d31">IDvdControl::ButtonSelectAndActivate</a>
 

 

