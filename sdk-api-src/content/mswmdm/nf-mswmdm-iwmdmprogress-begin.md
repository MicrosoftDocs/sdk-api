---
UID: NF:mswmdm.IWMDMProgress.Begin
title: IWMDMProgress::Begin (mswmdm.h)
description: The Begin method indicates that an operation is beginning. An estimate of the duration of the operation is provided when possible.
helpviewer_keywords: ["Begin","Begin method [windows Media Device Manager]","Begin method [windows Media Device Manager]","IWMDMProgress interface","IWMDMProgress interface [windows Media Device Manager]","Begin method","IWMDMProgress.Begin","IWMDMProgress::Begin","IWMDMProgressBegin","mswmdm/IWMDMProgress::Begin","wmdm.iwmdmprogress_begin"]
old-location: wmdm\iwmdmprogress_begin.htm
tech.root: WMDM
ms.assetid: 207b7cb5-4471-4be9-8252-9d467d67d7a2
ms.date: 12/05/2018
ms.keywords: Begin, Begin method [windows Media Device Manager], Begin method [windows Media Device Manager],IWMDMProgress interface, IWMDMProgress interface [windows Media Device Manager],Begin method, IWMDMProgress.Begin, IWMDMProgress::Begin, IWMDMProgressBegin, mswmdm/IWMDMProgress::Begin, wmdm.iwmdmprogress_begin
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
 - IWMDMProgress::Begin
 - mswmdm/IWMDMProgress::Begin
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
 - IWMDMProgress.Begin
---

# IWMDMProgress::Begin


## -description

The <b>Begin</b> method indicates that an operation is beginning. An estimate of the duration of the operation is provided when possible.

## -parameters

### -param dwEstimatedTicks [in]

<b>DWORD</b> specifying the estimated number of ticks that are needed for the operation to complete.

## -returns

The application should return one of the following <b>HRESULT</b> values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The operation should continue.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WMDM_E_USER_CANCELLED</b></dt>
</dl>
</td>
<td width="60%">
Windows Media Device Manager should cancel the current operation without waiting for it to finish. If the application is using block mode, then Windows Media Device Manager will return this error to the application.

</td>
</tr>
</table>

## -remarks

This operation is called by various methods to indicate that an operation is beginning. The number of ticks passed in <i>dwEstimatedTicks</i> is an estimate of how many ticks are needed for the operation to complete. During the course of the operation, the <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress-progress">Progress</a> method is called to indicate how many ticks have transpired. Applications can use the estimate to configure display mechanisms that show progress.

The <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress3-begin3">IWMDMProgress3::Begin3</a> method provides more information about what action is occurring.


#### Examples

The following C++ code is an implementation of the <b>Begin</b> method.


```cpp

HRESULT Begin(DWORD  dwEstimatedTicks)
{
    // TODO: Display the message: "IWMDMProgress::Begin called.: "
    // followed by the dwEstimatedTicks value.
    return S_OK;
}

```

## -see-also

<a href="/windows/desktop/WMDM/enabling-notifications">Enabling Notifications</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress">IWMDMProgress Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress3-begin3">IWMDMProgress3::Begin3</a>