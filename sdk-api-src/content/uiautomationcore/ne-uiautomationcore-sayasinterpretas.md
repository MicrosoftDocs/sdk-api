---
UID: NE:uiautomationcore.SayAsInterpretAs
title: SayAsInterpretAs
author: windows-sdk-content
description: Defines the values that indicate how a text-to-speech engine should interpret specific data.
old-location: winauto\uiauto_SayAsInterpretAs.htm
tech.root: WinAuto
ms.assetid: 70F6AA0E-52CB-49D4-BBAF-2B6367D5E44D
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: SayAsInterpretAs, SayAsInterpretAs enumeration [Windows Accessibility], SayAsInterpretAs_Address, SayAsInterpretAs_Alphanumeric, SayAsInterpretAs_Cardinal, SayAsInterpretAs_Currency, SayAsInterpretAs_Date, SayAsInterpretAs_Date_DayMonth, SayAsInterpretAs_Date_DayMonthYear, SayAsInterpretAs_Date_MonthDay, SayAsInterpretAs_Date_MonthDayYear, SayAsInterpretAs_Date_MonthYear, SayAsInterpretAs_Date_Year, SayAsInterpretAs_Date_YearMonth, SayAsInterpretAs_Date_YearMonthDay, SayAsInterpretAs_Media, SayAsInterpretAs_Name, SayAsInterpretAs_Net, SayAsInterpretAs_None, SayAsInterpretAs_Number, SayAsInterpretAs_Ordinal, SayAsInterpretAs_Spell, SayAsInterpretAs_Telephone, SayAsInterpretAs_Time, SayAsInterpretAs_Time_HoursMinutes12, SayAsInterpretAs_Time_HoursMinutes24, SayAsInterpretAs_Time_HoursMinutesSeconds12, SayAsInterpretAs_Time_HoursMinutesSeconds24, SayAsInterpretAs_Url, uiautomationcore/ SayAsInterpretAs_Address, uiautomationcore/ SayAsInterpretAs_Date_DayMonth, uiautomationcore/ SayAsInterpretAs_Net, uiautomationcore/ SayAsInterpretAs_Url, uiautomationcore/SayAsInterpretAs, uiautomationcore/SayAsInterpretAs_Alphanumeric, uiautomationcore/SayAsInterpretAs_Cardinal, uiautomationcore/SayAsInterpretAs_Currency, uiautomationcore/SayAsInterpretAs_Date, uiautomationcore/SayAsInterpretAs_Date_DayMonthYear, uiautomationcore/SayAsInterpretAs_Date_MonthDay, uiautomationcore/SayAsInterpretAs_Date_MonthDayYear, uiautomationcore/SayAsInterpretAs_Date_MonthYear, uiautomationcore/SayAsInterpretAs_Date_Year, uiautomationcore/SayAsInterpretAs_Date_YearMonth, uiautomationcore/SayAsInterpretAs_Date_YearMonthDay, uiautomationcore/SayAsInterpretAs_Media, uiautomationcore/SayAsInterpretAs_Name, uiautomationcore/SayAsInterpretAs_None, uiautomationcore/SayAsInterpretAs_Number, uiautomationcore/SayAsInterpretAs_Ordinal, uiautomationcore/SayAsInterpretAs_Spell, uiautomationcore/SayAsInterpretAs_Telephone, uiautomationcore/SayAsInterpretAs_Time, uiautomationcore/SayAsInterpretAs_Time_HoursMinutes12, uiautomationcore/SayAsInterpretAs_Time_HoursMinutes24, uiautomationcore/SayAsInterpretAs_Time_HoursMinutesSeconds12, uiautomationcore/SayAsInterpretAs_Time_HoursMinutesSeconds24, winauto.uiauto_SayAsInterpretAs
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - HeaderDef
api_location:
 - UIAutomationCore.h
api_name:
 - SayAsInterpretAs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

