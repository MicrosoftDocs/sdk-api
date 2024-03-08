---
UID: NF:wmp.IWMPEvents3.StringCollectionChange
title: IWMPEvents3::StringCollectionChange (wmp.h)
description: The StringCollectionChange event occurs when a string collection changes.
helpviewer_keywords: ["IWMPEvents3 interface [Windows Media Player]","StringCollectionChange method","IWMPEvents3.StringCollectionChange","IWMPEvents3::StringCollectionChange","IWMPEvents3StringCollectionChange","StringCollectionChange","StringCollectionChange method [Windows Media Player]","StringCollectionChange method [Windows Media Player]","IWMPEvents3 interface","wmp.iwmpevents3_iwmpevents3__stringcollectionchange","wmp/IWMPEvents3::StringCollectionChange"]
old-location: wmp\iwmpevents3_iwmpevents3__stringcollectionchange.htm
tech.root: WMP
ms.assetid: 93880116-e354-49d0-ba02-391fbb4d3f8c
ms.date: 4/26/2023
ms.keywords: IWMPEvents3 interface [Windows Media Player],StringCollectionChange method, IWMPEvents3.StringCollectionChange, IWMPEvents3::StringCollectionChange, IWMPEvents3StringCollectionChange, StringCollectionChange, StringCollectionChange method [Windows Media Player], StringCollectionChange method [Windows Media Player],IWMPEvents3 interface, wmp.iwmpevents3_iwmpevents3__stringcollectionchange, wmp/IWMPEvents3::StringCollectionChange
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11.
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
req.dll: Wmp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPEvents3::StringCollectionChange
 - wmp/IWMPEvents3::StringCollectionChange
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPEvents3.StringCollectionChange
---

# IWMPEvents3::StringCollectionChange


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>StringCollectionChange</b> event occurs when a string collection changes.

## -parameters

### -param pdispStringCollection [in]

Pointer to the <b>IDispatch</b> interface that represents the string collection that changed. Call <b>QueryInterface</b> to retrieve a pointer to <b>IWMPStringCollection</b>.

### -param change [in]

<a href="/windows/desktop/api/wmp/ne-wmp-wmpstringcollectionchangeeventtype">WMPStringCollectionChangeEventType</a> value indicating the type of change that occurred.

### -param lCollectionIndex [in]

The index of the string collection item that changed.

## -remarks

To receive <b>StringCollectionChange</b> events, you must obtain your string collection as follows:

<ol>
<li>Call <a href="/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_mediacollection">IWMPLibrary::get_mediaCollection</a> to get an <b>IWMPMediaCollection</b> interface.</li>
<li>Call the <a href="/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getattributestringcollection">getAttributeStringCollection</a> method of the interface you obtained in step 1.</li>
</ol>
If you obtain your <b>IWMPMediaCollection</b> interface by calling <a href="/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_mediacollection">IWMPCore::get_mediaCollection</a>, you will not receive <b>StringCollectionChange</b> events.

You can also handle this event through an <b>IDispatch</b> event sink by using the <b>_WMPOCXEvents</b> interface.

<b>Windows Media Player 10 Mobile: </b>This event is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpevents3">IWMPEvents3 Interface</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection">IWMPStringCollection Interface</a>



<a href="/windows/desktop/WMP/-wmpocxevents-interface">_WMPOCXEvents Interface</a>