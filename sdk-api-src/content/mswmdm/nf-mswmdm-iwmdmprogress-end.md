---
UID: NF:mswmdm.IWMDMProgress.End
title: IWMDMProgress::End (mswmdm.h)
description: The End method indicates that an operation is finished.
helpviewer_keywords: ["End","End method [windows Media Device Manager]","End method [windows Media Device Manager]","IWMDMProgress interface","IWMDMProgress interface [windows Media Device Manager]","End method","IWMDMProgress.End","IWMDMProgress::End","IWMDMProgressEnd","mswmdm/IWMDMProgress::End","wmdm.iwmdmprogress_end"]
old-location: wmdm\iwmdmprogress_end.htm
tech.root: WMDM
ms.assetid: 0edddd8c-8144-40dc-801c-eb8c899be249
ms.date: 12/05/2018
ms.keywords: End, End method [windows Media Device Manager], End method [windows Media Device Manager],IWMDMProgress interface, IWMDMProgress interface [windows Media Device Manager],End method, IWMDMProgress.End, IWMDMProgress::End, IWMDMProgressEnd, mswmdm/IWMDMProgress::End, wmdm.iwmdmprogress_end
req.header: mswmdm.h
req.include-header: 
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
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMDMProgress::End
 - mswmdm/IWMDMProgress::End
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IWMDMProgress.End
---

# IWMDMProgress::End


## -description

The <b>End</b> method indicates that an operation is finished.



## -returns

The return value from the method is ignored by Windows Media Device Manager.

## -remarks

This method is called by various interfaces to indicate that an operation is ending. Windows Media Device Manager ignores any return code returned by the <b>End</b> method because the operation is completed or terminated before this method is called.


#### Examples

The following C++ code is an implementation of the <b>End</b> method


```cpp

HRESULT End()
{
    // TODO: Display the message: "IWMDMProgress::End called."
    return S_OK; // Unnecessary, since this is ignored.
}

```

## -see-also

<a href="/windows/desktop/WMDM/enabling-notifications">Enabling Notifications</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress">IWMDMProgress Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress2-end2">IWMDMProgress2::End2</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress3-end3">IWMDMProgress3::End3</a>
