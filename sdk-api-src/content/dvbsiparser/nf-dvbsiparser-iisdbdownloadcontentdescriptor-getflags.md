---
UID: NF:dvbsiparser.IIsdbDownloadContentDescriptor.GetFlags
title: IIsdbDownloadContentDescriptor::GetFlags (dvbsiparser.h)
description: Gets flag values from an Integrated Services Digital Broadcasting (ISDB) download content descriptor.
helpviewer_keywords: ["GetFlags","GetFlags method [Microsoft TV Technologies]","GetFlags method [Microsoft TV Technologies]","IIsdbDownloadContentDescriptor interface","IIsdbDownloadContentDescriptor interface [Microsoft TV Technologies]","GetFlags method","IIsdbDownloadContentDescriptor.GetFlags","IIsdbDownloadContentDescriptor::GetFlags","dvbsiparser/IIsdbDownloadContentDescriptor::GetFlags","mstv.iisdbdownloadcontentdescriptor_getflags"]
old-location: mstv\iisdbdownloadcontentdescriptor_getflags.htm
tech.root: mstv
ms.assetid: df104d6d-1436-4c7d-b250-b740e1f70c07
ms.date: 12/05/2018
ms.keywords: GetFlags, GetFlags method [Microsoft TV Technologies], GetFlags method [Microsoft TV Technologies],IIsdbDownloadContentDescriptor interface, IIsdbDownloadContentDescriptor interface [Microsoft TV Technologies],GetFlags method, IIsdbDownloadContentDescriptor.GetFlags, IIsdbDownloadContentDescriptor::GetFlags, dvbsiparser/IIsdbDownloadContentDescriptor::GetFlags, mstv.iisdbdownloadcontentdescriptor_getflags
req.header: dvbsiparser.h
req.include-header: Dvbsiparser.idl
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
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
 - IIsdbDownloadContentDescriptor::GetFlags
 - dvbsiparser/IIsdbDownloadContentDescriptor::GetFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IIsdbDownloadContentDescriptor.GetFlags
---

# IIsdbDownloadContentDescriptor::GetFlags


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets flag values from an Integrated Services Digital Broadcasting (ISDB) download content descriptor.

## -parameters

### -param pfReboot [out]

Receives the value of the reboot flag. This flag is 1 if a reboot is required after the download, or 0 if it is not.

### -param pfAddOn [out]

Receives the value of the add_on flag. This flag is 1 if the download is added to an existing file, or 0 if the download overwrites the existing file.

### -param pfCompatibility [out]

Receives the value of the compatibility_flag field. This flag is 1 if the descriptor has a compatibility descriptor, or 0 if it does not.

### -param pfModuleInfo [out]

Receives the value of the module_info flag. This flag is 1 if the descriptor information for each module, or 0 if it does not.

### -param pfTextInfo [out]

Receives the value of the text_info_flag field. This flag is 1 if the descriptor includes a text description in its last field, or 0 if it does not.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbdownloadcontentdescriptor">IIsdbDownloadContentDescriptor</a>