---
UID: NF:mfidl.IMFTranscodeSinkInfoProvider.SetOutputFile
title: IMFTranscodeSinkInfoProvider::SetOutputFile (mfidl.h)
author: windows-sdk-content
description: Sets the name of the encoded output file.
old-location: mf\imftranscodesinkinfoprovider_setoutputfile.htm
tech.root: medfound
ms.assetid: 048d1822-9349-4d49-a468-c89bc9c51583
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFTranscodeSinkInfoProvider interface [Media Foundation],SetOutputFile method, IMFTranscodeSinkInfoProvider.SetOutputFile, IMFTranscodeSinkInfoProvider::SetOutputFile, SetOutputFile, SetOutputFile method [Media Foundation], SetOutputFile method [Media Foundation],IMFTranscodeSinkInfoProvider interface, mf.imftranscodesinkinfoprovider_setoutputfile, mfidl/IMFTranscodeSinkInfoProvider::SetOutputFile
ms.topic: method
f1_keywords: ["mfidl/IMFTranscodeSinkInfoProvider.SetOutputFile"]
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFTranscodeSinkInfoProvider.SetOutputFile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFTranscodeSinkInfoProvider::SetOutputFile


## -description


Sets the name of the encoded output file.


## -parameters




### -param pwszFileName [in]

Pointer to a null-terminated string that contains the name of the output file.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The media sink will create a local file with the specified file name.

Alternately, you can call <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftranscodesinkinfoprovider-setoutputbytestream">IMFTranscodeSinkInfoProvider::SetOutputByteStream</a> to specify a byte stream  that will receive the transcoded data. These two methods are mutually exclusive.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imftranscodesinkinfoprovider">IMFTranscodeSinkInfoProvider</a>
 

 

