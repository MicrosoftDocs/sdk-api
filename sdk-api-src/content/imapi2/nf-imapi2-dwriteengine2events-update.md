---
UID: NF:imapi2.DWriteEngine2Events.Update
title: DWriteEngine2Events::Update (imapi2.h)
description: Implement this method to receive progress notification of the current write operation. (DWriteEngine2Events.Update)
helpviewer_keywords: ["DWriteEngine2Events interface [IMAPI]","Update method","DWriteEngine2Events.Update","DWriteEngine2Events::Update","Update","Update method [IMAPI]","Update method [IMAPI]","DWriteEngine2Events interface","imapi.dwriteengine2events_update","imapi2/DWriteEngine2Events::Update"]
old-location: imapi\dwriteengine2events_update.htm
tech.root: imapi
ms.assetid: efee838d-aa6e-41a0-aafb-64ba6ca19f29
ms.date: 12/05/2018
ms.keywords: DWriteEngine2Events interface [IMAPI],Update method, DWriteEngine2Events.Update, DWriteEngine2Events::Update, Update, Update method [IMAPI], Update method [IMAPI],DWriteEngine2Events interface, imapi.dwriteengine2events_update, imapi2/DWriteEngine2Events::Update
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
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
 - DWriteEngine2Events::Update
 - imapi2/DWriteEngine2Events::Update
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - DWriteEngine2Events.Update
---

# DWriteEngine2Events::Update


## -description

Implement this method to receive progress notification of the current write operation.

## -parameters

### -param object [in]

The <a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2">IWriteEngine2</a> interface that initiated the write operation. 

This parameter is a <b>MsftWriteEngine2</b> object in script.

### -param progress [in]

An <a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2eventargs">IWriteEngine2EventArgs</a> interface that you use to determine the progress of the write operation. 

This parameter is a <b>MsftWriteEngine2</b> object in script.

## -returns

Return values are ignored.

## -remarks

Notifications are sent in response to calling the <a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-writesection">IWriteEngine2::WriteSection</a> method.

Notification is sent:

<ul>
<li>Once before the operation begins</li>
<li>Every 0.5 seconds during the write operation</li>
<li>Once after the operation completes</li>
</ul>
To stop the write process, call the <a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-cancelwrite">IWriteEngine2::CancelWrite</a> method.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-dwriteengine2events">DWriteEngine2Events</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-writesection">IWriteEngine2::WriteSection</a>



<a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2eventargs">IWriteEngine2EventArgs</a>
