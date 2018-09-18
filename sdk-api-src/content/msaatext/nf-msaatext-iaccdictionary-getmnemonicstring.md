---
UID: NF:msaatext.IAccDictionary.GetMnemonicString
title: IAccDictionary::GetMnemonicString
author: windows-sdk-content
description: Retrieves a mnemonic string.Note  Active Accessibility Text Services is deprecated.
old-location: winauto\iaccdictionary_iaccdictionary__getmnemonicstring.htm
tech.root: WinAuto
ms.assetid: 4855acea-83a9-4752-a780-7f0350a7b137
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: GetMnemonicString, GetMnemonicString method [Windows Accessibility], GetMnemonicString method [Windows Accessibility],IAccDictionary interface, IAccDictionary interface [Windows Accessibility],GetMnemonicString method, IAccDictionary.GetMnemonicString, IAccDictionary::GetMnemonicString, _msaa_IAccDictionary_GetMnemonicString, msaa.iaccdictionary_iaccdictionary__getmnemonicstring, msaatext/IAccDictionary::GetMnemonicString, winauto.iaccdictionary_iaccdictionary__getmnemonicstring
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msaatext.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Msaatext.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msaatext.dll
api_name:
 - IAccDictionary.GetMnemonicString
product: Windows
targetos: Windows
req.typenames: 
req.redist: Active Accessibility 2.0 RDK on Windows NT 4.0 with SP6 and later and Windows 98
---

# IAccDictionary::GetMnemonicString


## -description


Retrieves a mnemonic string.
<div class="alert"><b>Note</b>  Active Accessibility Text Services is deprecated. Please see     
<a href="http://go.microsoft.com/fwlink/p/?linkid=131573">Microsoft Windows Text Services Framework</a>for more information on advanced text input and natural language technologies.
		</div><div> </div>

## -parameters




### -param Term [in]

Type: <b>REFGUID</b>

A GUID representing a property.


### -param pResult [out]

Type: <b>BSTR*</b>

A mnemonic string for the property. This string is not localized.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If successful, returns S_OK.




## -remarks



If the <i>Term</i> parameter is not found in the dictionary, then <i>pResult</i> will be <b>NULL</b>.



