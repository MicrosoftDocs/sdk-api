---
UID: NF:mswmdm.IWMDeviceManager.GetRevision
title: IWMDeviceManager::GetRevision (mswmdm.h)
description: The GetRevision method retrieves the version number of Windows Media Device Manager currently in use.
helpviewer_keywords: ["GetRevision","GetRevision method [windows Media Device Manager]","GetRevision method [windows Media Device Manager]","IWMDeviceManager interface","IWMDeviceManager interface [windows Media Device Manager]","GetRevision method","IWMDeviceManager.GetRevision","IWMDeviceManager::GetRevision","IWMDeviceManagerGetRevision","mswmdm/IWMDeviceManager::GetRevision","wmdm.iwmdevicemanager_getrevision"]
old-location: wmdm\iwmdevicemanager_getrevision.htm
tech.root: WMDM
ms.assetid: 3ecb84cc-eaa5-436c-b5f1-50705462b88b
ms.date: 12/05/2018
ms.keywords: GetRevision, GetRevision method [windows Media Device Manager], GetRevision method [windows Media Device Manager],IWMDeviceManager interface, IWMDeviceManager interface [windows Media Device Manager],GetRevision method, IWMDeviceManager.GetRevision, IWMDeviceManager::GetRevision, IWMDeviceManagerGetRevision, mswmdm/IWMDeviceManager::GetRevision, wmdm.iwmdevicemanager_getrevision
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
 - IWMDeviceManager::GetRevision
 - mswmdm/IWMDeviceManager::GetRevision
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
 - IWMDeviceManager.GetRevision
---

# IWMDeviceManager::GetRevision


## -description

The <b>GetRevision</b> method retrieves the version number of Windows Media Device Manager currently in use.

## -parameters

### -param pdwRevision [out]

Pointer to a <b>DWORD</b> specifying the Windows Media Device Manager version number. Windows Media Device Manager 10 returns 0x00080000.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager">IWMDeviceManager Interface</a>