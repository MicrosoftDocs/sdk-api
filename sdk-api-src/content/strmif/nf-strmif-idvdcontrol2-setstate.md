---
UID: NF:strmif.IDvdControl2.SetState
title: IDvdControl2::SetState (strmif.h)
description: The SetState method saves the current disc position and state of the DVD Navigator filter.
old-location: dshow\idvdcontrol2_setstate.htm
tech.root: DirectShow
ms.assetid: 3941b469-46f3-4499-9062-81a873a36292
ms.date: 12/05/2018
ms.keywords: IDvdControl2 interface [DirectShow],SetState method, IDvdControl2.SetState, IDvdControl2::SetState, IDvdControl2SetState, SetState, SetState method [DirectShow], SetState method [DirectShow],IDvdControl2 interface, dshow.idvdcontrol2_setstate, strmif/IDvdControl2::SetState
f1_keywords:
- strmif/IDvdControl2.SetState
dev_langs:
- c++
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvdControl2::SetState


## -description



The <code>SetState</code> method saves the current disc position and state of the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator</a> filter.




## -parameters




### -param pState [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdstate">IDvdState</a> interface on the object that contains the state information.


### -param dwFlags [in]

Bitwise OR of one or more flags from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ne-strmif-dvd_cmd_flags">DVD_CMD_FLAGS</a> enumeration, specifying how to synchronize the command.


### -param ppCmd [out]

Receives a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdcmd">IDvdCmd</a> object that can be used to synchronize DVD commands. The caller must release the interface. This parameter can be <b>NULL</b>. For more information, see <a href="https://docs.microsoft.com/windows/desktop/DirectShow/synchronizing-dvd-commands">Synchronizing DVD Commands</a>.


## -returns



Returns S_OK if successful, or an <b>HRESULT</b> value otherwise.




## -remarks



The DVD Navigator uses the location information in the given state object to restore the playback position to a specific location on the disc.

This method is demonstrated in the DVDSample application in <b>CDvdCore::RestoreBookmark</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2 Interface</a>
 

 

