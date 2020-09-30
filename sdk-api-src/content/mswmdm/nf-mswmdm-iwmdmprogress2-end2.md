---
UID: NF:mswmdm.IWMDMProgress2.End2
title: IWMDMProgress2::End2 (mswmdm.h)
description: The End2 method extends IWMDMProgress::End by providing a completion status indicator.
helpviewer_keywords: ["End2","End2 method [windows Media Device Manager]","End2 method [windows Media Device Manager]","IWMDMProgress2 interface","IWMDMProgress2 interface [windows Media Device Manager]","End2 method","IWMDMProgress2.End2","IWMDMProgress2::End2","IWMDMProgress2End2","mswmdm/IWMDMProgress2::End2","wmdm.iwmdmprogress2_end2"]
old-location: wmdm\iwmdmprogress2_end2.htm
tech.root: WMDM
ms.assetid: 85265eb7-0702-4890-b6cb-b247296fe392
ms.date: 12/05/2018
ms.keywords: End2, End2 method [windows Media Device Manager], End2 method [windows Media Device Manager],IWMDMProgress2 interface, IWMDMProgress2 interface [windows Media Device Manager],End2 method, IWMDMProgress2.End2, IWMDMProgress2::End2, IWMDMProgress2End2, mswmdm/IWMDMProgress2::End2, wmdm.iwmdmprogress2_end2
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
 - IWMDMProgress2::End2
 - mswmdm/IWMDMProgress2::End2
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
 - IWMDMProgress2.End2
---

# IWMDMProgress2::End2


## -description

The <b>End2</b> method extends <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress-end">IWMDMProgress::End</a> by providing a completion status indicator.

## -parameters

### -param hrCompletionCode [in]

The return value of the operation that ended.

## -returns

The return value from the method is ignored by Windows Media Device Manager.

## -remarks

<b>IWMDMProgress2</b> is a callback interface provided by the application to Windows Media Device Manager for a particular operation. <b>End2</b> is called when that operation is completed. The <i>hrCompletionCode</i> parameter is the completion status of the operation that was in progress. For example, an application can provide an <b>IWMDMProgress2</b> interface pointer to the <b>Insert2</b> method. When the file transfer done by <b>Insert2</b> is completed, <b>End2</b> is called on the <b>IWMDMProgress2</b> interface pointer with the completion status of the file transfer as the <i>hrCompletion</i> parameter.


<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress3-end3">IWMDMProgress3::End3</a> provides more information, and should be implemented instead of this method.


#### Examples

The following C++ code is a simple implementation of the <b>Progress2</b> method.


```cpp

HRESULT Progress(DWORD  dwTranspiredTicks)
{
    // TODO: Display the message: "IWMDMProgress::Progress called." 
    // followed by the dwTranspiredTicks value.
    return S_OK;
}

```

## -see-also

<a href="/windows/desktop/WMDM/enabling-notifications">Enabling Notifications</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2">IWMDMProgress2 Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress3-end3">IWMDMProgress3::End3</a>