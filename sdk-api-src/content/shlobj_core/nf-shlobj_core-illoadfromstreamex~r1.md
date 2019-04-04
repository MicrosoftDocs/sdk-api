---
UID: NF:shlobj_core.ILLoadFromStreamEx~r1
title: ILLoadFromStreamEx
ms.date: 01/30/19
ms.keywords: ILLoadFromStreamEx
ms.topic: language-reference
targetos: Windows
product: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: shlobj_core.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - 
api_location:
 - shlobj_core.h
api_name:
 - ILLoadFromStreamEx
---

# ILLoadFromStreamEx function


## -description

<p class="CCE_Message">[<b>ILLoadFromStreamEx(IStream*, PIDLIST_RELATIVE*)</b> 
    is available for use in the operating systems specified in the Requirements section. It may be altered or 
    unavailable in subsequent versions.]

Loads an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> from an 
    <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>.


## -parameters

### -param pstm

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> interface from which the  
      <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> loads.


### -param ppidl

Type: <b>PIDLIST_RELATIVE*</b>

When this method returns and succeeds, contains the resulting relative 
      <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a>. If it fails, contains 
      <b>NULL</b>.


## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.


## -remarks

## -see-also

