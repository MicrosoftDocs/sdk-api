---
UID: NF:strmif.IDvdControl.AngleChange
title: IDvdControl::AngleChange
author: windows-sdk-content
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Sets the new display angle.
old-location: dshow\idvdcontrol_anglechange.htm
tech.root: DirectShow
ms.assetid: 4a91f05d-1ded-4ecb-8850-5ee7faad134d
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: AngleChange, AngleChange method [DirectShow], AngleChange method [DirectShow],IDvdControl interface, IDvdControl interface [DirectShow],AngleChange method, IDvdControl.AngleChange, IDvdControl::AngleChange, IDvdControlAngleChange, dshow.idvdcontrol_anglechange, strmif/IDvdControl::AngleChange
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
 - IDvdControl.AngleChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvdControl::AngleChange


## -description



<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="https://msdn.microsoft.com/eda43b20-1c4d-4769-bb87-3942716af13c">IDvdControl2</a> instread.</div>
<div> </div>
Sets the new display angle.




## -parameters




### -param ulAngle [in]

Value of the new angle, which must be from 1 through 9.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



This method returns an error unless the domain is DVD_DOMAIN_VideoManagerMenu, DVD_DOMAIN_VideoTitleSetMenu, DVD_DOMAIN_Title, or DVD_DOMAIN_Stop. For more information, see <a href="https://msdn.microsoft.com/2763a159-d4de-44c2-905b-5828f328cbd2">DVD_DOMAIN</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/a6ca0fe8-84e3-43e6-9421-29dcff056dfd">IDvdControl Interface</a>
 

 

