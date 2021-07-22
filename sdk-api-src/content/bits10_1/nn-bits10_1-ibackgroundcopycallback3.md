---
UID: NN:bits10_1.IBackgroundCopyCallback3
title: IBackgroundCopyCallback3 (bits10_1.h)
description: Clients implement the IBackgroundCopyCallback3 interface to receive notification that ranges of a file have completed downloading.
helpviewer_keywords: ["IBackgroundCopyCallback3","IBackgroundCopyCallback3 interface [BITS]","IBackgroundCopyCallback3 interface [BITS]","described","bits.ibackgroundcopycallback3","bits10_1/IBackgroundCopyCallback3"]
old-location: bits\ibackgroundcopycallback3.htm
tech.root: Bits
ms.assetid: 74712770-BB14-4B8A-8DA4-096CEB58D820
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyCallback3, IBackgroundCopyCallback3 interface [BITS], IBackgroundCopyCallback3 interface [BITS],described, bits.ibackgroundcopycallback3, bits10_1/IBackgroundCopyCallback3
req.header: bits10_1.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits10_0.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyCallback3
 - bits10_1/IBackgroundCopyCallback3
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits.lib
 - Bits.dll
api_name:
 - IBackgroundCopyCallback3
---

# IBackgroundCopyCallback3 interface


## -description

Clients implement the <b>IBackgroundCopyCallback3</b> interface to receive notification that ranges of a file have completed downloading.

Instead of polling for the download status of a file, clients use this interface.
To receive notifications, call the <a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setnotifyinterface">IBackgroundCopyJob::SetNotifyInterface</a> method to specify the interface pointer to your <a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopycallback">IBackgroundCopyCallback</a> implementation. To specify which notifications you want to receive, call the <a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setnotifyflags">IBackgroundCopyJob::SetNotifyFlags</a> method.
You must implement all methods of this interface and the <a href="/windows/desktop/api/bits3_0/nn-bits3_0-ibackgroundcopycallback2">IBackgroundCopyCallback2</a> and <b>IBackgroundCopyCallback</b> interface. For example, if you do not register for the file transferred callback, your <a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibackgroundcopycallback2-filetransferred">FileTransferred</a> method must still return <b>S_OK</b>. If you do not want to receive the file ranges   transferred callback, you can simply implement the <b>IBackgroundCopyCallback</b> or <b>IBackgroundCopyCallback2</b> instead.

## -inheritance

The <b>IBackgroundCopyCallback3</b> interface inherits from <a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopycallback">IBackgroundCopyCallback</a> and <a href="/windows/desktop/api/bits3_0/nn-bits3_0-ibackgroundcopycallback2">IBackgroundCopyCallback2</a>. <b>IBackgroundCopyCallback3</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopycallback">IBackgroundCopyCallback</a>



<a href="/windows/desktop/api/bits3_0/nn-bits3_0-ibackgroundcopycallback2">IBackgroundCopyCallback2</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setnotifyflags">IBackgroundCopyJob::SetNotifyFlags</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setnotifyinterface">IBackgroundCopyJob::SetNotifyInterface</a>
