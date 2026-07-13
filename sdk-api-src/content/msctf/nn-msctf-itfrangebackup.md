---
UID: NN:msctf.ITfRangeBackup
title: ITfRangeBackup (msctf.h)
description: The ITfRangeBackup interface is implemented by the TSF manager and is used by a text service to create a backup copy of the data contained in a range object.
helpviewer_keywords: ["ITfRangeBackup","ITfRangeBackup interface [Text Services Framework]","ITfRangeBackup interface [Text Services Framework]","described","_tsf_itfrangebackup_ref","msctf/ITfRangeBackup","tsf.itfrangebackup"]
old-location: tsf\itfrangebackup.htm
tech.root: TSF
ms.assetid: f98cd8d0-7033-4bd2-94a1-1a75913c2647
ms.date: 12/05/2018
ms.keywords: ITfRangeBackup, ITfRangeBackup interface [Text Services Framework], ITfRangeBackup interface [Text Services Framework],described, _tsf_itfrangebackup_ref, msctf/ITfRangeBackup, tsf.itfrangebackup
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfRangeBackup
 - msctf/ITfRangeBackup
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfRangeBackup
---

# ITfRangeBackup interface


## -description

The <b>ITfRangeBackup</b> interface is implemented by the TSF manager and is used by a text service to create a backup copy of the data contained in a range object. This backup copy can be used later to restore the range object. An instance of this interface is obtained by calling <a href="/windows/desktop/api/msctf/nf-msctf-itfcontext-createrangebackup">ITfContext::CreateRangeBackup</a>.

## -inheritance

The <b>ITfRangeBackup</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfRangeBackup</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-itfcontext-createrangebackup">ITfContext::CreateRangeBackup
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfrange-clone">ITfRange::Clone
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="/windows/desktop/TSF/ranges">Ranges: Clones and Backups</a>
