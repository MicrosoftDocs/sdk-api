---
UID: NN:wuapi.IUpdate
title: IUpdate (wuapi.h)
description: Contains the properties and methods that are available to an update. (IUpdate)
helpviewer_keywords: ["IUpdate","IUpdate interface [Windows Update Agent]","IUpdate interface [Windows Update Agent]","described","wua.iupdate","wuapi/IUpdate"]
old-location: wua\iupdate.htm
tech.root: wua
ms.assetid: d0feee2a-96f6-4c86-aaf8-f49d05616fc9
ms.date: 12/05/2018
ms.keywords: IUpdate, IUpdate interface [Windows Update Agent], IUpdate interface [Windows Update Agent],described, wua.iupdate, wuapi/IUpdate
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUpdate
 - wuapi/IUpdate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IUpdate
---

# IUpdate interface


## -description

Contains the properties and methods that are available to an update.

## -inheritance

The <b>IUpdate</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IUpdate</b> also has these types of members:

## -remarks

If the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_bundledupdates">BundledUpdates</a> property contains an <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatecollection">IUpdateCollection</a>, some properties and methods of the update may only be available on the bundled updates, for example, <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_downloadcontents">DownloadContents</a> or <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdate-copyfromcache">CopyFromCache</a>.
