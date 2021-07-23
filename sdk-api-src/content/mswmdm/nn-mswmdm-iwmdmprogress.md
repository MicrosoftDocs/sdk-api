---
UID: NN:mswmdm.IWMDMProgress
title: IWMDMProgress (mswmdm.h)
description: The optional, application-implemented IWMDMProgress allows an application to track the progress of operations, such as formatting media or file transfers.
helpviewer_keywords: ["IWMDMProgress","IWMDMProgress interface [windows Media Device Manager]","IWMDMProgress interface [windows Media Device Manager]","described","IWMDMProgressInterface","mswmdm/IWMDMProgress","wmdm.iwmdmprogress"]
old-location: wmdm\iwmdmprogress.htm
tech.root: WMDM
ms.assetid: 9af022a6-19b4-41b7-b951-0acad6aab4a2
ms.date: 12/05/2018
ms.keywords: IWMDMProgress, IWMDMProgress interface [windows Media Device Manager], IWMDMProgress interface [windows Media Device Manager],described, IWMDMProgressInterface, mswmdm/IWMDMProgress, wmdm.iwmdmprogress
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMDMProgress
 - mswmdm/IWMDMProgress
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mswmdm.h
api_name:
 - IWMDMProgress
---

# IWMDMProgress interface


## -description

The optional, application-implemented <b>IWMDMProgress</b> allows an application to track the progress of operations, such as formatting media or file transfers. This interface is submitted to, and called by, the <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorageglobals">IWMDMStorageGlobals</a> and <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol">IWMDMStorageControl</a> interfaces.

These methods do not provide a way for the application to know which operation is being tracked. However, the <b>IWMDMProgress3</b> methods do provide a means to identify the operation; if possible, you should implement that interface instead.

## -inheritance

The <b>IWMDMProgress</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMDMProgress</b> also has these types of members:

## -see-also

<a href="/windows/desktop/WMDM/enabling-notifications">Enabling Notifications</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2">IWMDMProgress2 Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3">IWMDMProgress3 Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol">IWMDMStorageControl Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorageglobals">IWMDMStorageGlobals Interface</a>



<a href="/windows/desktop/WMDM/interfaces-for-applications">Interfaces for Applications</a>
