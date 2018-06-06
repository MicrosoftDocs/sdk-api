---
UID: NE:msctf.__MIDL_ITfTextLayoutSink_0001
title: "__MIDL_ITfTextLayoutSink_0001"
author: windows-sdk-content
description: Elements of the TfLayoutCode enumeration specify the type of layout change in an ITfTextLayoutSink::OnLayoutChange notification.
old-location: tsf\tflayoutcode.htm
old-project: TSF
ms.assetid: b9ff6d11-68f2-47c5-b8d7-b3bc2533fdbb
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: TF_LC_CHANGE, TF_LC_CREATE, TF_LC_DESTROY, TfLayoutCode, TfLayoutCode enumeration [Text Services Framework], __MIDL_ITfTextLayoutSink_0001, _tsf_tflayoutcode_ref, msctf/TF_LC_CHANGE, msctf/TF_LC_CREATE, msctf/TF_LC_DESTROY, msctf/TfLayoutCode, tsf.tflayoutcode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: MsClus.tlb
tech.root: 
req.typenames: TfLayoutCode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Msctf.h
api_name:
 - TfLayoutCode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# __MIDL_ITfTextLayoutSink_0001 enumeration


## -description


Elements of the <b>TfLayoutCode</b> enumeration specify the type of layout change in an <a href="https://msdn.microsoft.com/a99313ab-98a7-4fc0-b3ae-78ff26a41d8e">ITfTextLayoutSink::OnLayoutChange</a> notification.


## -enum-fields




### -field TF_LC_CREATE

The view has just been created.


### -field TF_LC_CHANGE

The view layout has changed.


### -field TF_LC_DESTROY

The view is about to be destroyed.


## -remarks



In TSF, a view is on-screen rendering of document content. These constants are assigned to parameters of methods of the <b>ITf*</b> interfaces, but not those of the <b>IText*</b> interfaces.




## -see-also




<a href="https://msdn.microsoft.com/a99313ab-98a7-4fc0-b3ae-78ff26a41d8e">ITfTextLayoutSink::OnLayoutChange
      </a>
 

 

