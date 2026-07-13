---
UID: NF:mswmdm.IMDSPStorageGlobals.Initialize
title: IMDSPStorageGlobals::Initialize (mswmdm.h)
description: The Initialize method formats the storage medium. (IMDSPStorageGlobals.Initialize)
helpviewer_keywords: ["IMDSPStorageGlobals interface [windows Media Device Manager]","Initialize method","IMDSPStorageGlobals.Initialize","IMDSPStorageGlobals::Initialize","IMDSPStorageGlobalsInitialize","Initialize","Initialize method [windows Media Device Manager]","Initialize method [windows Media Device Manager]","IMDSPStorageGlobals interface","mswmdm/IMDSPStorageGlobals::Initialize","wmdm.imdspstorageglobals_initialize"]
old-location: wmdm\imdspstorageglobals_initialize.htm
tech.root: WMDM
ms.assetid: 661060dc-5a38-4110-80f6-c67e3be8c96b
ms.date: 12/05/2018
ms.keywords: IMDSPStorageGlobals interface [windows Media Device Manager],Initialize method, IMDSPStorageGlobals.Initialize, IMDSPStorageGlobals::Initialize, IMDSPStorageGlobalsInitialize, Initialize, Initialize method [windows Media Device Manager], Initialize method [windows Media Device Manager],IMDSPStorageGlobals interface, mswmdm/IMDSPStorageGlobals::Initialize, wmdm.imdspstorageglobals_initialize
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
 - IMDSPStorageGlobals::Initialize
 - mswmdm/IMDSPStorageGlobals::Initialize
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
 - IMDSPStorageGlobals.Initialize
---

# IMDSPStorageGlobals::Initialize


## -description

The <b>Initialize</b> method formats the storage medium. This method is optional. However, this method should be implemented if the device supports this functionality. If this method is not implemented, <a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getcapabilities">IMDSPStorageGlobals::GetCapabilities</a> must return WMDM_STORAGECAP_NOT_INITIALIZABLE in addition to any other flags. For more information, see <a href="/windows/desktop/WMDM/mandatory-and-optional-interfaces">Mandatory and Optional Interfaces</a>.

## -parameters

### -param fuMode [in]

Mode used to initialize the medium. Specify exactly one of the following two modes. If both modes are specified, block mode is used.

<table>
<tr>
<th>Mode
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>WMDM_MODE_BLOCK</td>
<td>The operation is performed using block mode processing. The call is not returned until the operation is finished.</td>
</tr>
<tr>
<td>WMDM_MODE_THREAD</td>
<td>The operation is performed using thread mode processing. The call returns immediately and the operation is performed in a background thread.</td>
</tr>
</table>

### -param pProgress [in]

Pointer to an <b>IWMDMProgress</b> interface implemented by an application to track the progress of the formatting operation. This parameter can be <b>NULL</b>.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

If WMDM_MODE_BLOCK is specified, <b>Initialize</b> does not return until formatting is finished. If the WMDM_MODE_THREAD is specified, the call returns immediately and the caller can use the <b>IMDSPStorageGlobals::GetStatus</b> method to track the initializing operation.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorageglobals">IMDSPStorageGlobals Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getcapabilities">IMDSPStorageGlobals::GetCapabilities</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getstatus">IMDSPStorageGlobals::GetStatus</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress">IWMDMProgress Interface</a>
