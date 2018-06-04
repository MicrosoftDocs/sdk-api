---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
---

# IPenInputPanel::put_Factoid


## -description



Deprecated.  The <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a> has been replaced by the <a href="https://msdn.microsoft.com/867f2d6f-e63a-4c02-9370-3848a3b5c40a">Text Input Panel (TIP)</a>.

Gets or sets the string name of the factoid used by the <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a> object.



This property is read/write.


## -parameters


## -remarks



A factoid provides a recognizer context for ink within a particular field. You specify a factoid if an input field is of a known type. For example, if the input field contains a date, specify the <a href="https://msdn.microsoft.com/library/windows/hardware/hh406437">Date</a> factoid.

For more information about factoids and how to use them, see <a href="https://msdn.microsoft.com/b64f6856-453c-4080-84e0-0a9e69e79de7">Using Context to Improve Accuracy</a>. For a list of possible values for the <b>Factoid</b> property, see <a href="https://msdn.microsoft.com/9d5fc370-ba58-438b-8850-f31f0f0f6608">Supported Factoids from Version 1</a>.

<div class="alert"><b>Note</b>  String representations of factoids are case-sensitive.</div>
<div> </div>
This property has no effect on keypads or keyboards.

The <a href="https://msdn.microsoft.com/247a1f7d-8205-4e4d-9cfc-daad9bd2191f">WordList</a> factoid is not supported for the <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a> object.

The default value for the <b>Factoid</b> property is DEFAULT. In locales that use recognizers of Latin script, all factoids may be used. In locales that use recognizers of East Asian characters, the following factoid values are relevant:

<ul>
<li>
            DIGIT: Implies the Num bias button on the East Asian writing pad.</li>
<li>
            ONECAHR: Implies the Alpha bias button on the East Asian writing pad.</li>
<li>Common <a href="https://msdn.microsoft.com/247a1f7d-8205-4e4d-9cfc-daad9bd2191f">factoids</a> (JapaneseCommon, ChineseSimpleCommon, ChineseTraditionalCommon, KoreanCommon, KanjiCommon, and HangulCommon) imply the Alpha/Num bias button on the East Asian writing pad.</li>
</ul>
All factoid values other than DIGIT and ONECHAR are interpreted as the common factoid that is appropriate for the current input locale.

If the <b>Factoid</b> property is set, it is forwarded to the recognizer only if the <a href="https://msdn.microsoft.com/4098525c-8d29-419a-9484-9e70420416bc">SetInputScope</a> function has not also been called.




## -see-also




<a href="https://msdn.microsoft.com/247a1f7d-8205-4e4d-9cfc-daad9bd2191f">Factoid Constants</a>



<a href="tablet.ipeninputpanel">IPenInputPanel</a>



<a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a>
 

 

