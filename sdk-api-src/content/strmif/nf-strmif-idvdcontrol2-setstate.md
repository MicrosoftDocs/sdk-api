---
UID: NF:strmif.IDvdControl2.SetState
title: IDvdControl2::SetState
author: windows-sdk-content
description: The SetState method saves the current disc position and state of the DVD Navigator filter.
old-location: dshow\idvdcontrol2_setstate.htm
old-project: DirectShow
ms.assetid: 3941b469-46f3-4499-9062-81a873a36292
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IDvdControl2 interface [DirectShow],SetState method, IDvdControl2.SetState, IDvdControl2::SetState, IDvdControl2SetState, SetState, SetState method [DirectShow], SetState method [DirectShow],IDvdControl2 interface, dshow.idvdcontrol2_setstate, strmif/IDvdControl2::SetState
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IDvdControl2.SetState
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDvdControl2::SetState


## -description



The <code>SetState</code> method saves the current disc position and state of the <a href="https://msdn.microsoft.com/3b2c01a2-d52c-4497-8fc9-d1113e8507e8">DVD Navigator</a> filter.




## -parameters




### -param pState [in]

Pointer to the <a href="https://msdn.microsoft.com/df30a3b9-7541-42a8-b642-3b6450a0345e">IDvdState</a> interface on the object that contains the state information.


### -param dwFlags [in]

Bitwise OR of one or more flags from the <a href="https://msdn.microsoft.com/05eb5ab8-a1b3-4876-bac3-29510af8cdbd">DVD_CMD_FLAGS</a> enumeration, specifying how to synchronize the command.


### -param ppCmd [out]

Receives a pointer to an <a href="https://msdn.microsoft.com/85f9b208-ddc2-4d9c-a30b-b666c81a49d2">IDvdCmd</a> object that can be used to synchronize DVD commands. The caller must release the interface. This parameter can be <b>NULL</b>. For more information, see <a href="https://msdn.microsoft.com/37e8f940-617d-43f6-92bd-aadccafe0059">Synchronizing DVD Commands</a>.


## -returns



Returns S_OK if successful, or an <b>HRESULT</b> value otherwise.




## -remarks



The DVD Navigator uses the location information in the given state object to restore the playback position to a specific location on the disc.

This method is demonstrated in the DVDSample application in <b>CDvdCore::RestoreBookmark</b>.




## -see-also




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/eda43b20-1c4d-4769-bb87-3942716af13c">IDvdControl2 Interface</a>
 

 

