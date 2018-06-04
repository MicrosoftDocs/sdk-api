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

# SayAsInterpretAs enumeration


## -description


Defines the values that indicate how a text-to-speech engine should interpret specific data.


## -enum-fields




### -field SayAsInterpretAs_None

The text should be spoken using the default for the text-to-speech engine.


### -field SayAsInterpretAs_Spell

The text should be spoken character by character.


### -field SayAsInterpretAs_Cardinal

The text is an integral or decimal number and should be spoken as a cardinal number.


### -field SayAsInterpretAs_Ordinal

The text is an integral number and should be spoken as an ordinal number.


### -field SayAsInterpretAs_Number

The text should be spoken as a number.


### -field SayAsInterpretAs_Date

The text should be spoken as a date.


### -field SayAsInterpretAs_Time

The text should be spoken as a time value.


### -field SayAsInterpretAs_Telephone

The text should be spoken as a telephone number.


### -field SayAsInterpretAs_Currency

The text should be spoken as currency.


### -field SayAsInterpretAs_Net

The text should be spoken as a network address, including saying the '\', '/', and '@' characters.


### -field SayAsInterpretAs_Url

The text should be spoken as a URL.


### -field SayAsInterpretAs_Address

The text should be spoken as an address.


### -field SayAsInterpretAs_Alphanumeric

The text should be spoken as an alphanumeric number.


### -field SayAsInterpretAs_Name

The text should be spoken as a name.


### -field SayAsInterpretAs_Media

The text should be spoken as media.


### -field SayAsInterpretAs_Date_MonthDayYear

The text should be spoken as a date in a Month/Day/Year format.


### -field SayAsInterpretAs_Date_DayMonthYear

The text should be spoken as a date in a Day/Month/Year format.


### -field SayAsInterpretAs_Date_YearMonthDay

The text should be spoken as a date in a Year/Month/Day format.


### -field SayAsInterpretAs_Date_YearMonth

The text should be spoken as a date in a Year/Month format.


### -field SayAsInterpretAs_Date_MonthYear

The text should be spoken as a date in a Month/Year format.


### -field SayAsInterpretAs_Date_DayMonth

The text should be spoken as a date in a Day/Month format.


### -field SayAsInterpretAs_Date_MonthDay

The text should be spoken as a date in a Month/Day format.


### -field SayAsInterpretAs_Date_Year

The text should be spoken as a date in a Year format.


### -field SayAsInterpretAs_Time_HoursMinutesSeconds12

The text should be spoken as a time value in an Hours:Minutes:Seconds 12-hour format.


### -field SayAsInterpretAs_Time_HoursMinutes12

The text should be spoken as a time value in an Hours:Minutes 12-hour format.


### -field SayAsInterpretAs_Time_HoursMinutesSeconds24

The text should be spoken as a time value in an Hours:Minutes:Seconds 24-hour format.


### -field SayAsInterpretAs_Time_HoursMinutes24

The text should be spoken as a time value in an Hours:Minutes 24-hour format.

